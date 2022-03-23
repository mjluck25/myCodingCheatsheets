# HTML Forms

- is responsible for collecting information to send somewhere else.

## How a FORM works

- `HTTP Request` 
  - instructs the receiving computer how to handle the incoming information.
- `action` attribute
  - determines **where** the info is sent.
- `method` attribute
  - is assigned an **HTTP verb** that is included in the HTTP request.
  - ie. POST, GET, PUT, PATCH, DELETE
  - note that these verbs does not necessarily need to be capitalized but is capitalized by convention.

## Text Input

`type` attribute

- default value is `text` where the user can type any text in the input field.

`name` and `value` attribute

- the name attribute is necessary when submitting the form since `name=value` will be sent to the html file.
- the value attribute creates a pre-filled value in the form.
- the `value` is also what gets POSTed when the form is submitted.

## Adding a Label

- to properly identify an input we use the appropriately named `label` element.
- needs an opening and closing tag.
- to associate a `label` to an `input`, the input needs an ID.
- the `for` attribute of the label will then be assigned with the value of the ID of the input.

## Password Input

`type` attribute

- value will be `password`.
- this will replace text with asterisk or dots.

## Number Input

`type` attribute

- value will be `number`.
- limits the input into numbers and a few special characters like -, +, and .

`step` attribute

- creates arrows inside the input field to increase or decrease by the value of the step attribute.

## Range Input

`type` attribute

- value is `range`.
- to limit what numbers our users could type we might consider using a different type value.
- creates a slider with `min/max` attributes to set its min and max values.
- to control the smoothness of the slider, we can add a `step` attribute.

## Checkbox Input

`type` attribute

- value is `checkbox`.
- gives multiple options to users and allow them to select any number of options.
- the checkboxes can be grouped through similar values of the `name` attribute.
- `values` assigned to the checkboxes are not visible in the form but the identification of each checkbox will be through the `label`.

## Radio Button Input

`type` attribute

- value is `radio`.
- to present multiple options and only allow for one selection.
- the options are grouped by having the same value of the `name` attribute.

## Dropdown List

`select` element

- creates an organized list for a large number of `options`.

`option` element

- to populate the dropdown list, we add multiple `option` elements each with a `value` attribute within the `select` element.

## Datalist Input

`datalist` element

- placed within a **text-input-type**.
- the input creates a text field where users can type in and filter options from the `datalist`.

`list` attribute

- the datalist is associated to the input element via the `list` attribute within the input element.
- the id attribute of the `datalist` element is of the same value of the `list` attribute.

## Textarea Element

- creates a bigger text field for a larger input of information.

`rows` and `cols` attribute

- to set how many lines of row and columns will be the size of the field.

## Submit Form

`type` attribute

- value is `submit`.

`value` attribute

- value displayed within the button.
- `Submit` text is the default value.