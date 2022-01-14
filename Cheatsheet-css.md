# CSS - Cascading Style Sheets

- responsible for styling the Web
- _HTML_: Structure while _CSS_: Layout, Look
- General syntax: selector `{property:value;property:value}`

## Three ways to use CSS

1. **Inline CSS**

   - most basic but not that used
     > ie. `<h1 style="color:red"></h>`
   - it overwrites internal and external css style

2. **Internal CSS**

   - better to use than inline but lacks flexibility in working with multiple pages
   - within the head element:
     > ie. `<style> element1{designated:style} element2</style>`
   - it overwrites external style

3. **External CSS**
   - better in working with multiple files
   - create a `.css` file inside the folder
   - add in the head element:
     - we use the `link` element to link the HTML and CSS files together
       > `<link rel="stylesheet" href="style.css">`
     - `rel` attribute: describes the relationship between the HTML file and the CSS file.
     - `href` attribute: acts like an anchor element and describes the path or address to the CSS file.

---

Comment

- `/* */`

---

### CSS Rule/Syntax

> ie. e1 {color:red; font-size: 3rem;}

- SELECTOR: `e1` where we select an element and inputs a style for that element
- DECLARATION BLOCK: everything enclosed by the curly braces `{}`
- DECLARATION: the group name for a `property:value` pair that applies a style to the selected element
- PROPERTY: visual characteristic of the element to be modified (ie. `color` and `font-size`)
- VALUE: value of the property (ie.`red` and `3rem`)
- always end with semicolon per `property:value` pair

Grouping Selectors

> ie. h1 and h2 --> h1, h2 {}

- use a comma (without space) per element to be grouped and styled

Type Selector

- selects the type of the html element that you would like to style
- such as `h1`, `h2`, `p`, `body`, etc.

ID Selector (`#`)

- selects the value of an `id` attribute within an element
- always starts with hash sign before the given id attribute value
- id's should always be unique
  > ie. html: `<h1 id="title">Title Book</h1>`
  > css: `#title {property:value;}`
- can only have a single value

Class Selector (`.`)

- selects the value of an `class` attribute within an element
- always starts with dot sign before the given class attribute value
  > ie. html: `<h1 class="green">Title Book</h1>`
  > css: `.green {property:value;}`
- can add multiple classes separated by a space

Attribute Selector (`element[attr]`)

- matches elements based on the presence or value of a given attribute

`element[attr]`

- Represents elements with an attribute name of `attr`.

`element[attr=value]`

- Represents elements with an attribute name of `attr` whose value is exactly `value`.

`element[attr~=value]`

- Represents elements with an attribute name of `attr` whose value is a whitespace-separated list of words, one of which is exactly `value`.

`element[attr|=value]`

- Represents elements with an attribute name of `attr` whose value can be exactly `value` or can begin with `value` immediately followed by a hyphen, `-` (U+002D). It is often used for language subcode matches.

`element[attr^=value]`

- Represents elements with an attribute name of `attr` whose value is prefixed (preceded) by `value`.

`element[attr$=value]`

- Represents elements with an attribute name of `attr` whose value is suffixed (followed) by `value`.

`element[attr*=value]`

- Represents elements with an attribute name of `attr` whose value contains at least one occurrence of `value` within the string.

Universal Selector (`*`)

- least amount of specificity
- we use this whenever we want to reset a default browser style
- usually used for:
  > box-sizing: border-box;
  > margin: 0;

Pseudo class Selector (`:`)

- keyword added to a selector that specifies a special state of the selected element(s).
- most common pseudo class:
`:focus`
`:visited`
`:hover`
`:disabled`
`:active`
- [list of pseudo classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

Inheritance, Parent, Children

- to select children within a parent
  > ie. ul li a {}
  > selects all links within the lists within the unordered list

Div/Span

- both are used for grouping elements to be styled
  - `<div></div>`: mostly used to style as a block element, it also starts in a new line
  - `<span></span>`: mostly used to style as an inline element

Last Rule and Specificity

- last rule always applies but if the selector is specific, it will be applied

### Color Properties

- there are _140_ color names
  > "color: value;" sets the foreground color
  > "background-color: value;" sets  the background color
  > "background: color value;"

#### Color specification/format

1. **RGB** _(0-255)_

   > ie. color: rgb(255, 255, 255); === white

   - Opacity/Transparency _(0-1)_
     > ie. background: rgba(r,g,b,0.5)

2. **HEX Values** _(#RRGGBB)_

   - values are as follows:
     - 123456789 A(10) B(11) C(12) D(13) E(14) F(15)
       > ie. #FF0000 is Red and #00FF00 is Green

3. **HSL** (_Hue, Saturation, Light_)
   - _Hue_: measured in degrees of the color circle (0-360)
   - _Saturation_: Saturation percent (full saturation is 100%, 0% is shade of gray)
   - _Light_: lightness percent (100% is white, 50% is normal, 0% is black)

- [random color palettes](coolors.co)

---

### CSS Properties and corresponding Units

#### Absolute value

- does not depend on anything (like size of screen or window)
- pixel or px
  > ie. font-size: 200px; width: 200px; height: 500px;

#### Relative value

- value will depend on the (value of) parent element

1. percentage or %

   > ie. width: 100%; height: 50%;

2. em

   - 1em = 16px --> default browser style
   - 1em is the base value

3. rem

   - depends on the value of the root and not the parent
   - 1rem = 16px --> default browser style
   - 1rem is the base value

4. vh/vw

   - view height and view width
   - depends on the size of the screen (percent of the screen)
   - usually used in creating banners

---

Google Developer tools & Default browser styles

- Right click on page then click inspect

Calc Function (`calc()`)

- perform math operations
- mix and match values
- syntax: there should be a space in between operators

### Typography

`font-family` property

- adds a font style to a text

`font-stack`

- adds multiple font style in case the browser doesn't support the selected font style
- it allows a generic font-family
  - such as serif, sans-serif, cursive, fantasy and monospace

google fonts

- search google fonts and you can pick and import different fonts to the browser
- can either import or copy and paste the code to the stylesheet

`font-weight`

- bold, bolder, lighter

`font-style`

- inherit, italic, normal, oblique

`text-align`

- alignment of the text
- center, justify, left, right

`text-indent`

- indention of the text
- accepts multiple values such as px, em, rem, etc.

`line-height`

- controls the space in between the lines

`letter-spacing`

- controls the spaces in between letters

`word-spacing`

- controls the spaces in between words

`text-transform`

- transforms text
- capitalize (capitalize first letter of all words), uppercase (capitalize all letters), lowercase (lower case all letters)

`text-decoration`

- decorates the text
- line-through, overline, underline, etc.

---

## CSS Box Model

> CONTENT >> PADDING >> BORDER >> MARGIN

`padding`

- controls the padding or margin around the content
- distance from the content to the edge of the element
- top, bottom, left, right
  > ie. padding-left, padding-right, etc.
  > ie. padding: value; --> padding size all around the element
  > ie. padding: top/bottom left/right; --> padding: 30px 50px;
  > ie. padding: top right bottom left; --> padding: 30px 20px 50px 40px;

`margin`

- distance from the screen or elements to the another element
- same syntax with the padding
- can be negative margin
- horizontal centering a block element
- make the margin auto
  - margin: auto;

`border`

- border around the edge of an element
- border-style: style of the border
- border-width: width of the border
- border-color: color of width
- syntax: `border: width style color;`
- border radius
  - changes the corners to round corners

---

### Outline

> CONTENT >> BORDER >> OUTLINE >> MARGIN

- same syntax with the border
- difference with border is the offset property
  - `outline-offset`: --> offsets the outline from the element

---

### Display Property (`display:`)

block

- always starts a new line and takes full width
- top/bottom margin is respected

inline

- does not start a new line and only take up as much as content space
- top/bottom margin is not respected

inline block

- for the top/bottom margin to be respected and display the element in only one line

none

- does not display the element
- totally take out an element

---

`box-sizing: border-box;`

- so that any other padding that is added will be within the element

Opacity property (`opacity:`)

- controls the transparency of an element
- the max value is 1 and minimum is 0

Visibility property (`visibility:`)

- controls the visibility of an element
- hidden or visible

---

### Background property (`background:`)

background-repeat

- set by default
- values: `repeat`, `no-repeat`, `repeat-x`, `repeat-y`, `space`, `round`

background-size

- values: `cover` (fills up the whole div regardless of its size);
  `contain` (keeps the ratio of the image); `auto`

background-position

- values: `center`, `left`, `right`, `top`, `bottom`, percentage of x and y
  > ie. of percentage: background-position: 50% 50%;

background-attachment

- values: `fixed` (image is fixed giving the scroll effect);

linear-gradient()

- creates a gradient of colors
- default is from bottom to top
  > ie. linear-gradient(yellow, green, blue)
- from top to bottom
  > ie. linear-gradient(to top, yellow, green, blue)
- from left/right
  - change `to top` with `left`/`right`
- from a certain degrees
  > ie. linear-gradient(150deg, yellow, green, blue)
- can also include rgba values for the colors
  > ie. background: linear-gradient(to top, rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.9));
- useful in overlaying background images for a clearer image
- search the net for: 'css linear generator' to generate different gradient combinations

**syntax shortcut for background property**

- `background: linear gradient(value, value), url(image location) <space> position/size <space> attachment value <space> repeat value`
  > ie. background: linear gradient(rgba(0,0,0,0.2),rgba(0,0,0,0.2)), url("./images/big-image.jpeg") center/cover no-repeat fixed;

---

Float/Clear property (`float:`/`clear:`)

- float property makes an image float
  - values: left or right
- clear property makes the floating image be respected by the next element and will be left alone to the next line
  - values: left, right or both

Overflow property (`overflow: hidden`)

- makes an image or other element be hidden when its size overflows from the given div or window

### Position property (`position:`)

- can also be: `top:` , `right:`, `bottom:` , `left:`

position: `static`

- normal flow of the document as written in code

position: `relative`

- sets the element's position relative to its original position

position: `absolute`

- sets the element's position relative to the position of its ancestor element with a relative position property

position: `fixed`

- set the element relative to the actual document

---

### Media Queries

- allow us to work with responsive designs
- allow us to style elements depending on the screen size
- will use mostly: `min-width` and `max-width`
- starts with `@media`
  >ie. @media screen and (min-width: 576px) {
  >        body {
  >             background: red;
  >             }
  >        .banner {
  >             background: yellow;
  >             }
  >        h1 {
  >             color: black;
  >           }
  >       `}
- syntax is very important for it to work!

---

z-index

- controls the z-axis (what's on top over the other ie. in multiple image overlays)
- default value is zero
- will only work if the position value is declared (`absolute` or `relative`); will not work if position is static

---

pseudo elements (`::before` `::after` CONTENT not element)

- Syntax: `elementType::before/::after{content: "";}`
- to add a content before/after another content
- does not work with images

---

### Basic Selectors (review)

Descendant and Child Combinators

- syntax for descendant: `ancestor/parent descendant{block of code}`
- syntax for direct children: `ancestor/parent > child{block of code}`

`element::first-line`

- selects the first line of the element

`element::first-letter`

- selects the first letter of the element

**note**: `:` is used in classes while `::` is used in pseudo elements

`element:hover`

- changes the element as you hover over it

#### Links

`a:link{}`

- selects all links to be styled

`a:visited`

- changes/styles the links as it is visited or clicked

`a:hover`

- changes/styles the links as you hover over it

`a:active`

- changes/styles the links as it is clicked on the spot

`:root{}`

- styling the root element of the document
- it usually is the html element
- usually used in applying general styles and css variables

---

### Transform property (`transform:`)

- applies some type of transformation to the element (such as `translational` to x-,y-,z-axis, `rotation`, `scaling` and `skewing`)

#### Functions of transform property

`translateX();` , `translateY();` , `translateZ();` , `translate();`

- translates the element to desired value

`scaleX();` , `scaleY();` , `scaleZ();` , `scale();`

- controls the scaling of an element with respect to x, y or z axis

`rotateX();` , `rotateY();` , `rotateZ();` , `rotate();`

- rotates the element to a certain angle (in degrees) along x, y or z axis

`skewX();` , `skewY();` , `skewZ();` , `skew();`

- skews the element to a certain angle (in degrees) along x, y or z axis

### Transition (`transition:`)

- in charge of making state changes occurring some period of time

`transition-property:`

- sets the property where the transition will occur
- can add multiple values separated by a comma

`transition-duration:`

- sets the duration of the transition of an element
- can add multiple values separated by a comma

`transition-timing-function:`

- values
  - `ease` = slow start, fast, slow end (this is the default transition)
  - `linear` = same speed start to end
  - `ease-in` = slow start
  - `ease-out` = slow end
  - `ease-in-out` = slow start, fast, slow end

`transition-delay:`

- sets the duration of the delay of the transition of an element

__syntax shortcut__:
  > transition: `property 1` `duration value` `timing value` `delay duration value` , `property 2` `duration value` `timing value` `delay duration value` , and so on;
  > transition: `all` `duration value` `timing value` `delay duration value`; (for all Properties)

### Animation property (`animation:`)

- change over time with points
- syntax/selector: `@keyframes` `name` `{}`
- multiple points using percentage(ie. 0%, 1%,2%,3%,...)

#### Functions

`animation-name`

- selects the name designated for animation

`animation-duration`

- sets the duration of the animation (in s or ms)

`animation-iteration-count` (without Units)

- sets the number of times the animation will play (can be infinite)

`animation-fill-Mode`

- to get the values you end up with (forwards/backwards)

__syntax shortcut__

- animation: `name` `duration` `iteration count`

---

### CSS Variables (Custom Properties)

- holds a value and reuse it
- syntax: `--varName: value`
- property: `var(--varName)`
- can be used globally (through :root{}) or locally (by element)

---

### Icons

- using [fontAwesome](fontawesome.com)
- copy the code from the website and paste it in the head element
- or download the icons and create a link manually in the HTML

---

`text-shadow:` / `box-shadow:`

- adds shadow on the text/box
- syntax: `x-axis value` `y-axis value` `blur value` `color`
- can use text/box-shadow generator and copy & paste the code

---

browser prefixes

- [autoprefixer](https://autoprefixer.github.io/)
- [canIUse](https://caniuse.com/)

---

### Emmet Abbreviation

- shortcuts in coding in html

classes

- use dot (.)
- `element.className1.className2`

ids

- use hashtag (#)
- `element#idName`

parent/child

- use angle bracket (>)
- `element1>element2>element3`

add multiple element

- use asterisk `*`
- `element*5`

add text within the element

- use curly braces `{}`
- `element{text}`

to remove extra space (whitespace) in html

- use `overflow-x: hidden;`

---

### CSS GRID

`display: grid;`

- grids can overlap one another

`grid-template-columns`

- creates a grid of columns of designated width
  > ie. grid-template-columns: 40% 30% 30%; or 60% 40%;
- fractional unit is recommended (`fr`)
  > ie. grid-template-columns: 1fr 1fr 1fr;
- using repeat(number of times, unit)
  > ie. grid-template-columns: repeat(4, 1fr 2fr);

`grid-gap`

- creates a gap inbetween rows and columns
  > ie. grid-gap: 5px;
  
  `grid-column-gap`
  - creates a gap between columns

  `grid-row-gap`
  - creates a gap between rows

`grid-auto-rows`

- sets the height of all rows
  > ie. grid-auto-rows: 100px;
- setting the height(to be flexible) to accommodate its content using `minmax()` function
  > ie. grid-auto-rows: minmax(100px, auto)

`justify-items` / `align-items`

- similar to flexbox justify-content
- values are: start, end, center and default value is stretch

`justify-self` / `align-self`

- adjust individual elements

`grid-column` / `grid-row`

- sets the element to the designated span of rows or columns
  > ie. grid-column: 1/3; means start from 1st line and end in 3rd line
