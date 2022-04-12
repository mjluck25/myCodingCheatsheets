
# Javascript

Packages to install (in code editor):

  1. Babel ES6/ES7
      - gives syntax highlighting
  2. Node.js Modules Intellisense
  3. Node.js extension pack
  4. VS code for node.js development pack

---

Table of Contents

1. [Adding Sequences in strings](#adding-sequences-in-strings)
1. [Arrays](#arrays)
1. [Comparison & Logical Operators](#comparison-operators)
1. [Conditional Statements](#conditional-statements)
1. [Data Types](#data-types-input-info)
1. [Destructuring](#destructuring)
1. [Escaping literal quotes in strings](#escaping-literal-quotes-in-strings)
1. [Events](#events)
1. [Functions](#functions)
1. [Iterables](#iterables)
1. [Javascript in HTML](#javascript-in-html)
1. [Loops](#loops)
1. [Objects](#objects)
1. [Others](#others)
1. [Scope](#scope)
1. [Sets](#sets)
1. [Variables](#variables)
1. [WORKING with NUMBERS](#working-with-numbers)

---

## Adding Sequences in strings

- `\n`: newline or linefeed (to advance downward to the next line.)
- `\r`: carriage return (moves the cursor to the beginning of the line without advancing to the next line.)
- `\tab`: tab
- `\b`: backspace
- `\f`: form feed (advance downward to the next "page".)

---

`.length` function

- to know the number of characters in a string

### bracket notation `[]`

- to find the index of a string
- also to store multiple values separated by a comma (called arrays)
  - nested arrays (bracket within a bracket of values)
  - can also be indexed
  - array indexes to modify data with that index
- to access the array of an array use double brackets notation
  - `[][]`

---

## Arrays

### Iterators

- are methods called on arrays to _manipulate elements_ and return values.
- _function declaration_, _function expression_ and _arrow function_ can be used to supply a callback function as an argument to the iterator.

1. **mutator** methods
    - methods that modify the original array

2. **accessor** methods
    - methods that return a new value or representation

#### `.forEach()` method

- will execute the same code for each element of an array.
- During each execution, the current element is passed as an argument to the callback function.
- return value for .forEach() will always be UNDEFINED.
- Another way to pass a callback for .forEach() is to use arrow function syntax.
- We can also define a function beforehand to be used as the callback function.

  ```javascript
  ie.
    function printGrocery(element){
      console.log(element);
  }
  groceries.forEach(printGrocery); //printGrocery is used as the callback function

  ```

#### `.map()` method

- takes an argument of a callback function and returns a new array.
- It doesn't modify the original array.

#### `.filter()` method

- returns a new array.
- returns an array of elements after filtering out certain elements from the original array.
- callback function for the .filter() method should return true or false depending on the element that is passed to it.
- The elements that cause the callback function to return true are added to the new array.
- It doesn't modify the array.

#### `.findIndex()` method

- to find the location of an element in an array.
- will return the index of the first element that evaluates to true in the callback function.
- `returns -1` if none of the elements in the array satisfies the condition.
- check a condition for each element of an array, until the condition is met, and get the index of the first array element that passes said condition.
- syntax: .findIndex(callBackFcn)

#### `.indexOf()` method

- find the index of the first occurrence of a specific value in an array.
  > Syntax: `arr.indexOf(searchElement, fromIndex)`

#### `.reduce()` method

- returns a single value after iterating through the elements of an array, thereby reducing the array.
- can also take an optional second parameter to set an initial value for accumulator (_remember, the first argument is the callback function!_).

  ```javascript
    .reduce((accumulator, currentValue) => {firstArg}, secondArg) 
    //accumulator is the firstArg, currentValue is secondArg
  ```

#### `.some()` method

- tests whether at least one element in the array passes the test implemented by the provided function.
- It returns true if, in the array, it finds an element for which the provided function returns true; otherwise it returns false.
- It doesn't modify the array.

#### `.every()` method

- tests whether all elements in the array pass the test implemented by the provided function.
- It returns a Boolean value.

#### `.includes()` method

- determines whether an array includes a certain value among its entries, returning true or false as appropriate.

#### `.find()` method

- returns the first value in an array that passes a given test.

#### `.slice()` method

- returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array.
- the original array will not be modified.

#### `.splice()` method

- changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

  ```javascript
  //Parameters:
    const arr = [];
    arr.splice(startIndex, deleteCount, ItemToAdd1, ItemToAdd2...)
  ```

### Array methods

`.push()`

- to insert or add values at the end of an array.

`.pop()`

- to remove the last value within an array.
- no value needed to insert.

`.shift()`

- removes the first value within an array.
- no value needed to insert.

`.unshift()`

- to insert or add values at the beginning of an array

---

## Comparison operators

- compare two values and return a boolean value.

Equality operator (`==`)

- often used in if statements.
- most common comparison operator that uses boolean statements.
- attempts to convert both values being compared to a common type.

Strict Equality operator (`===`)

- does not convert values being compared to a common type.
  
  ```javascript
  (ie. number === '123' //will return false
  ```

Inequality operator (`!=`)

Strict Inequality operator (`!==`)

greater than (`>`) or equal to (`>=`)

less than (`<`) or equal to (`<=`)

### Logical operators

- always evaluated from left to right

`And` operator (`&&`)

`Or` statement (`||`)

- can be used in short circuit evaluation (where setting a default value if the value being set is falsy)

```javascript
example:
let x = '';
let y = x || 'default'; //short circuit evaluation; will return the default value if x is false
```

`not` operator (`!`)

- also called `bang` operator.

### Short circuit Evaluation

- if the first condition is met, there is no need to evaluate the second condition.

---

## Conditional Statements

### If statement

```javascript
syntax:
if (condition){code to be executed}
else {};
```

- `{}`: executes the code in the curly brackets.
- `()`: conditions defined.

### Else statement

- alternate block of code to be executed if a given condition is not met

### Else if statement

- more than one condition.
- logical order is important (always call the first condition first then next).

### Switch statements

- tests the value and can have many case statements which defines various possible values.
- `default` statement: sets the value of the variable whenever the input data is not within the cases.
- `break`: breaks the code per case.

  ```javascript
  syntax: 
  switch(value){
    case 1:
      x = "some value";
      return x;
      break;
    case 2: 
      y = "some value";
      return y;
      break; 
    default: 
      z = "some value";
      return z;
      break;
  }
  ```

- multiple inputs give the same output (just omit the break statement and retain it in the last case).

### Ternary operator

- like a one line if-else expression

  ```javascript
  Syntax:
  condition ? `statement-if-true` : `statement-if-false`;
  //read like this: if condition, then (`?`) do this if true or do this if false.
  ```

---

## Data Types (input info)

- `undefined`:  not defined
- `null`: nothing
- `boolean`: answerable by true or false
- `string`: text
- `symbol`: unique character or value
- `number`: number
- `object`: can store a lot of different value pairs

---

## Destructuring

### Destructuring assignment of variables from arrays

- assignment of variables within the array is in order.

```javascript
Syntax:
[var1,var2,var3,,,,var7] = [a,b,c,d,e,f,g]
// var1 = a, var2 = b, var7 = g
// to access a specific element within the array, just add comma.
```

### Property Value Shorthand (ES6)

- a destructuring technique.
- we only use the key instead of assigning it a value of the parameter.

### Destructured assignment

- we create a variable with the name of an object’s key that is wrapped in curly braces `{ }` and assign to it the object.

  ```javascript
  Syntax:
    const object = {
    prop1: value1,
    prop2: value2
    }
  //To access the properties and store in a variable:
  const { prop2 } = object; 
  //no need to do: const prop2 = object.prop2
  ```

---

## Escaping literal quotes in strings

`\` (backslash)

- add a backslash (`\`) before the quotation marks.
- or use a single quotation mark (`'`)
- or use a tilde (`` ` ``)

- backticks (` `` `)
  - an ES6 feature that allows you to create strings in JS
  - **Template Literals**: are special type of string that makes reading complex strings easier.
  - used in string concatenation:

    ```js
    ie. 
    let number = 5 
    console.log(`${number} Articles`) //returns 5 Articles
    ```

  - can create multiline w/o using new line character (\n)

    ```js
    ie. console.log(`"Hello 
    
    
    Readers!!!"`) 
    /* returns 
    "Hello 
    

    Readers!!!" */
    
    ```

---

## Events

- are user interactions and browser manipulations that you can program to trigger functionality. Examples are:
  - A mouse clicking on a button
  - Webpage files loading in the browser
  - A user swiping right on an image

### Event handlers

- are fired to notify code of "interesting changes" that may affect code execution.
- These can arise from user interactions such as using a mouse or resizing a window, changes in the state of the underlying environment (e.g. low battery or media events from the operating system), and other causes.
- modify and update DOM elements after an event fires.
- [event types](https://developer.mozilla.org/en-US/docs/Web/Events)

#### `.addEventListener()`

- a DOM element listen for a specific event and execute a block of code when the event is detected.
  - **event target** is the DOM element that listens for an event.
  - **event handler** is the block of code that runs when the event happens.

  ```javascript
  Syntax:
    eventTarget.addEventListener('click', eventHandlerFunction)
  example:
    btn = document.getElementById('button')
    let return = () => {some code}
    
    btn.addEventListener('click', return)
  ```

#### `.onevent` property

- Syntax: `.on` + `lowercased event type name`
- ie. `onclick`, `onmouseover`, etc.
- allows for one event handler function to be attached to the event target.

  ```javascript
  Syntax:
    eventTarget.onevent = eventHandlerFunction
  example:
    btn = document.getElementById('button')
    let return = () => {some code}

    btn.onclick = return;
  ```

#### `.removeEventListener()`

- stops the event target from “listening” for an event to fire when it no longer needs to.
- takes in two arguments: (1) `event type as a string` and (2) `event handler function.`
- If .addEventListener() was provided an anonymous function, then that event listener cannot be removed.

  ```javascript
  Syntax:
    eventTarget.removeEventListener('click', eventHandlerFunction)
  example:
    btn = document.getElementById('button')
    let return = () => {
      btn.removeEventListener('click', return) //stops an event after being fired once
    }

    btn.addEventListener('click', return)
  ```

### Event Object Properties

- stores `events` as _Event objects_ with their related data and functionalities as properties and methods.
- When an event is triggered, the event object can be passed as an argument to the event handler function.

  ```javascript
  example: 
  function eventHandlerFunction(event){
    console.log(event.timeStamp);
  }
  
  eventTarget.addEventListener('click', eventHandlerFunction);
  ```

#### `.target` property

- to reference the element that the event is registered to.

#### `.type` property

- to access the name of the event.

#### `.timeStamp` property

- to access the number of milliseconds that passed since the document loaded and the event was triggered.

---

## Functions

`function()`

- creates a reusable code in js
- parameters can be passed in functions.
  - we can pass input data into the function using parameters or variables
  > ie. `functionName(param1, param2)`: param1 and param2 can be any variable you set.

### Parameters

- are the names listed in the function definition.
- in ES6, default parameters are added
  > ie. `function functionName (name = 'someName'){}`
  - Rest parameters `(...args)`
    - allows to create a function that creates a variable number of arguments.
  - Spread parameters `[...args]`
    - takes an array and spreads out into its individual arrays.

### Arguments

- are the real values passed to (and received by) the function.

```javascript
syntax(1): function functionName() {}
syntax(2): function() {} //anonymous function
syntax(3): () => {} //arrow function
syntax(4): (function() {})(); //self-invoking
```

### Anonymous functions

- functions that don't have a name.
- can be converted into arrow functions for easier writing.

### Arrow functions

- replaces the function keyword.
- are not well suited for defining object methods.
- work really well with higher order functions such as math, filter and reduce
  - _higher order functions_: take functions as arguments for processing collections of data.

### Concise body arrow functions

- with single parameter, there is no need for parenthesis.
- with 2 or more parameter or if the parameter is zero, parenthesis is needed.
- if function body is single line, return keyword and curly braces is not needed (also called as _implicit return_).

### Factory Functions

- is a function that returns an object and can be reused to make multiple object instances.
- can also have parameters allowing us to customize the object that gets returned.

  ```javascript
  Syntax:
  const factoryFunctionName = (param1, param2, etc.) = {
  return {param1: param1, param2: param2} 
  //return an object and uses the parameters as its values
  }
  const someVariableName = factoryFunctionName(param1, param2) 
  //invoke the factory function and store it to the variable with two parameters
  ```

### Higher order functions

- functions that accept other functions as arguments and/or return functions as output
- storing functions into a variable

  ```javascript
    const variableName = functionName; 
    //note that it doesn't have () at the end
    //We want to assign the value of the function itself, not the value it returns when invoked.
  ```

- functions are first class objects and can also have its own properties and methods(like `.name` or `.length`).

### Callback functions

- functions that get passed in as parameters and invoked within the block of the higher order function
- they get called during the execution of the higher-order function.
- we pass in the function itself by typing the function name without the parentheses (_that would evaluate to the result of calling the function_).

### Self-invoking functions

- executed automatically if the expression is followed by ().

### Hoisting

- allows access to function declarations before they’re defined.
- function expressions are not hoisted.

### pass-by-reference

- where we pass to a function a reference to where the variable memory is stored and changing the memory.
- common example are OBJECTS.

---

## Iterables

- Objects that can be iterated over with for..of are called iterable.
- see [for..of loops](#forof-loops)

### next() method

- an object becomes an iterator when this is implemented
- does not support for..of statement
- must return an object with two properties: value (next value) and done (boolean)
- `value`: the value returned by the iterator (can be omitted if done is true)
- `done`: TRUE if the iterator has completed and FALSE if the iterator has produced a new value

  ```javascript
  // Home Made Iterable
  function myNumbers() {
    let n = 0;
    return {
      next: function() {
        n += 10;
        return {value:n, done:false};
      }
    };
  }

  // Create Iterable
  const n = myNumbers();
  n.next(); // Returns 10
  n.next(); // Returns 20
  n.next(); // Returns 30
  ```

### Symbol.iterator

- a function that returns a next() function
- can be iterated over with code: `for (const x of iterable) {}`

  ```javascript
  myNumbers = {}
  myNumbers[Symbol.iterator] = function() {
    let n = 0;
    done = false;
    return {
      next() {n+=10;
      if (n==100){done=true}
      return {value:n, done:done}
      }
    }
  }
  // this code can now be used:
    for (const num of myNumbers) {}

  //manually, we can use this code:
  let iterator = myNumbers[Symbol.iterator]();

  while (true) {
    const result = iterator.next();
    if (result.done) break;
    // Any Code Here
  }
  ```

---

## Javascript in HTML

### `<script></script>` element

- applies the code inside this element to the HTML document.
- the code is **parsed sequentially** in HTML as how it is typed.
- if the javascript file is a separate file, this element should be within the `head` element.

### `src` attribute

- value is where the source or location of the javascript file.

### `defer` attribute

- no value needed.
- specifies scripts should be executed after the HTML file is completely parsed.
- it loads the script but defers the actual execution of the JavaScript until after it finishes parsing the rest of the elements in the HTML file.

### `async` attribute

- no value needed.
- the script will not wait until the entire page is parsed.
- it will execute immediately after it has been downloaded.
- useful for scripts that are independent of other scripts in order to function accordingly.

---

## Loops

### While Loops

- runs the same code multiple times while a certain condition is true and stops if it is false
- always checks first the condition before it runs the code within the Loop.

### Do While Loops

- will always run the code one time before it checks the condition.

### For Loops

- runs the same code multiple times given an initialization, condition, and final expression.

- `initialization`: first expression in the code. or where to start from.
- `condition`: iteration of the first expression. or how many times we want to execute.
- `final expression`: what will execute at each iteration.

### For..in Loops

- loops through the properties of an _object_.
- the block of code will be executed once for each property.
- returns the key element of the object or array.

### For..of loops

- loops through the values of iterable objects such as Arrays (from first to last item), Strings, Maps, NodeLists, etc.
- cannot be used to iterate in reverse.
- iterating a _string_

  ```javascript
  syntax: for (cons x of "some string") {`block of code`}
  ```

- iterating over an _array_

  ```javascript
  syntax: for (const x of [1,2,3,4,5]) {`block of code`}
  ```

`break` keyword

- terminates a loop.

`continue` keyword

- skip one iteration of a loop.

```javascript
  Syntax:
    //While loop
    while (condition) {code}; 
    // Do while loop
    do {statement} while (condition); 
    //for loop
    for (initialization; condition; final expression) {code};
    example: for (let i=0; i<3; i++) {console.log(i)} //returns 0 1 2
    // for..in loop
    for (let variable in object) {code};
    //for..of loop
    for (let item of array) {code};
```

---

## Objects

- similar to arrays but differ in using property in accessing data through curly braces `{}`.
- `property`: everything before a colon (`:`).

  ```javascript
  syntax: 
        const objectName = {"property1": "value1", "property2": "value2", etc..};
  ```

### Dot notation (`.property`)

- used to access object properties.
- `objectName.property1;`

### Bracket notation (`['property']`)

- also used to access object properties.
- required to be used if the property has spaces in it.
- also used in storing property in a variable.
- `objectName['property 1'];`

### Delete statement

- to delete a property from an object.

  ```javascript
  syntax:
        delete objectName.property1;
  ```

`.hasOwnProperty` method

- to check if the object has a property.

`JSON.parse(JSON.stringify(Object))`

- to create a copy of the original object.

`.freeze()` method

- prevents object from mutation or changing.

### Maps

- holds key-value pairs where keys can be any data-type.
- remembers the original insertion order of the keys.
- has a property that represents the size of the map.
- Being able to use objects as keys is an important Map feature.

### Privacy

- the idea that only certain properties should be mutable or able to change in value.
- common convention is to place an underscore _ before the name of a property to mean that the property should not be altered.

### Getters

- methods that get and return the internal properties of an object.
- we use the 'get' keyword
- getter methods do not need to be called with a set of parentheses.
- can perform an action on the data when getting a property.
- can return different values using conditionals.
- can access the properties of the calling object using this.
- when using getter (and setter) methods is that properties cannot share the same name as the getter/setter function.

### Setters

- reassign values of existing properties within an object.

### Some Built-in Object Properties

#### `Object.assign()` method

- copies all enumerable own properties from one or more source objects to a target object.
- It returns the modified target object.

  ```javascript
  Syntax:
    Object.assign(target, ...sources) //returns target object
  ie. 
    const someVariable = Object.assign({}, source1, {prop1: value1, prop2: value2})
  ```

#### `Object.entries()` method

- returns an array of the key-value pairs in an object passed as an argument.

  ```javascript
  Syntax:
    Object.entries(object);
  ```

#### `Object.keys(`method`)`

- returns an array of a given object's own enumerable property names, iterated in the same order that a normal loop would.

  ```javascript
  Syntax:
    Object.keys(object);
  ```

---

## Others

Comment

- `//`: in-line comment
- `/* */`: multi-line comment

Queue

- an abstract data structure where items are kept in order where new items can be added at the back of the queue while old items are taken off at the beginning of the queue.

JSON.stringify

- a way to change an array into a string that can easily be printed out in a screen.

`return` statement

- returns a value from a function.
- if the return statement is not declared, the return value will be _undefined_ and nothing will be returned by the function
- the execution of a function is stopped in a return statement where the code that follows it will not be executed.

  ```javascript
    ie. 
    function functionName(){return anyValue};
  ```

`Linting`

- a process by which text is evaluated and improved by an application.

---

## Scope

- refers to the visibility of variables
  
### Global scope

- variables defined outside a function block.
- can be seen throughout the js code.
- setting a variable without the "var" keyword automatically makes it global even if it's defined within a function.

### Local scope

- variables defined within a function as well as the function parameters.

---

## Sets

- a collection of unique values.
- each value can only occur once in a Set.
- can hold any value of any data type.

### Set methods

`new Set()`

- Creates a new Set.

`add()`

- Adds a new element to the Set.

`delete()`

- Removes an element from a Set.

`has()`

- Returns true if a value exists.

`clear()`

- Removes all elements from a Set.

`forEach()`

- Invokes a callback for each element.

`values()` / `keys()`

- Returns an Iterator with all the values in a Set
entries().
- Returns an Iterator with the [value,value] pairs from a Set.

### Property

`size`

- Returns the number of elements in a Set.

---

## Variables

`var` statement

- can be used throughout the whole program.
  > ie. `var` fruit = "banana"

global variable

- absence of `var` statement
  > ie. someText = "This text"
- syntax 2: someText = "some text"

`let` statement

- will only be used within the scope of where you declare them.
- doesn't let you declare the same variable twice.
   > ie. `let` someText = "some text"

`const` statement

- constant variable.
- a variable that should never change.
  
  ```js
  syntax:
  const myName = "Mart";
  const myName = "Jeremiah"; //this will have an error
  ```

`use strict`

- used to catch coding mistakes such as not declaring variable without using var, let and const keywords
- can be placed on top of full js file or within a function

---

`;` (semicolon)

- all lines in js should end with a semicolon
- Semicolons are used to separate executable JavaScript statements.

---

`console.log()`

- allows to run code and print into the console.

---

## WORKING with NUMBERS

`++` / `--`

- adding two plus/minus signs after a variable increments/decrements it by one

`decimal numbers`

- also known as `float`.

`%`

- modulus or remainder

`**`

- exponential.

`!=`

- not equal.

### Augmented addition/subtraction/multiplication/division

- `+=`: shortcut for addition.
- `-=`: shortcut for subtraction.
- `*=`: shortcut for multiplication.
- `/=`: shortcut for division.

### Math functions

`Math.random()`

- generates random decimal number between 0 and 1 but does not equal to max (which is 1 in this example).

  ```js
  Math.random() * 5; //returns random number between 0 and 5 but does not include 5.
  ```

`Math.floor()` / `Math.ceil()`

- rounds down / up to the nearest whole number.

  ```js
  Math.floor(1.7 * 2); //returns 3
  Math.ceil(1.7 * 2); //returns 4
  ```

### parseInt function

- converts a string into an integer.
- if the string cannot be converted into an integer, it will return "`NaN`" meaning "`not a number`".
- can also be used with a `radix`.
  - `radix`: specifies the base of the number in the string
  - such as base 2 (binary) or base 7 or base 8, base 10 (default)
    > syntax: `parseInt(str, radix)`  ie. parseInt("56", 2)

---
