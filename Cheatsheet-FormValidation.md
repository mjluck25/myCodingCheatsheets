# Form Validation

## Regular Expressions

- series of characters representing a pattern which recognized by computers.
- also known as __regex__ or __regexp__.
- `[^]*` syntax matches all of the expressions to a pattern.

## Client-side Validation: HTML

- `client` is the process interacting with the server on behalf of the user, inw the case of websites, the _web browsers_.
- examples of HTML code are using the `required`, `pattern = 'regexp pattern you want'`, `min/max` (for numbers), `min/maxlength` (for strings) attributes in the __input element__

## Client-side Validation: Javascript

- Client-side validation has two main advantages. First, it’s a better experience for the user to be alerted to problematic data immediately rather than having to wait for that information to come back from the server and have to fill out the form again. Second, catching mistakes earlier in the process saves the application time and resources as well. But not all issues can be handled with the built-in HTML validations.
- In order to truly customize validation or to perform more complex validations, we can incorporate JavaScript form validations. We can do this by either writing the JavaScript ourselves or by incorporating a JavaScript library. If we have unique requirements for usernames on our site, for example, we’ll have to provide these systems of validation ourselves.
- If we’re creating a relatively simple website, it makes sense to code the form validation ourselves or use a simple vanilla JavaScript library—just-validate, for example. But most basic validation libraries will involve directly accessing or manipulating the DOM. This can get tricky when working with a framework that relies on a virtual DOM—like React or Vue. In those situations, it might be best to incorporate a library that works well with your specific framework. For example, the formik library is a lightweight library that simplifies validating forms in a React app.

## Back-end Validation

- There are two main ways to validate inputs on the server-side.

  1. The first takes place while the user is still inputting data into the form on the front-end. We can make __asynchronous requests__ to the server with pieces of their data and send feedback directly to the user before they’ve submitted. This is slower than front-end validation and can be a design challenge from a user-experience perspective.

  1. The second is once the form has been submitted. Back-end form validation is our application’s last defense against problematic data, and it’s essential to verify the validity and safety of data before adding it to a database. This is also an opportunity to “sanitize” the data: in order for our database to be useful, it’s important that all data within it is formatted consistently. This means that while we may want to be flexible about the formatting we require from a user, we likely want to transform inputs into a strict format before entering them in the database.
