# Web Accessibility

## Contrast

- Enhancing contrast in _Headings_, _Font Choices_ and _Color_ can help us ensure that our site is accessible to users with vision impairments.

#### Headings accessibility

- proceed with the heading Hierarchy (h1 to h5).

#### Text accessibility

- Using ***real text*** instead of text within graphics provides a website with several key benefits:

  - screen readers can _transform_ the text into a _voice-over_
  - users can _scale_ or _magnify_ the text for better legibility without losing image quality
  - it’s _less taxing on the browser to load_ real text versus requesting large image assets from a server.

##### Color(background) and text

- high contrast between text and background.
- a ratio of at least **4.5:1** should be used on all standard text sizes.
- lighter color must have four and a half times the luminance of its paired darker color.
- A ratio of at least **3:1** should be used for larger text sizes.

##### Font size accessibility

- The standard font size for most modern web browsers is **16 pixels**.

#### Color accessibility

- contrast between elements in the foreground and those in the background.


## Semantic HTML Elements

- The quickest way of improving accessibility for screen readers is to use the appropriate tags for a given task.

## ARIA Role

- To help add context to web page information, ARIA provides an HTML attribute called _role_.
- The value of an element’s role changes how a screen reader communicates the element.

```html
for example:
<div id="code-editor" role="complementary">
  ...
</div>
```

- this [link](https://www.w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties) has a list of acceptable ARIA roles..

### ARIA properties

- are attributes that you can add to HTML elements.
- provide additional information about elements that might not be obvious to users of screen readers.
- Other ARIA properties are useful in more complex websites using HTML forms, JavaScript, and other advanced tools.
- [ARIA Techniques](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques)

`aria-label`

- an example of an ARIA property. 

### `alt` Attribute

- used to describe an image (or several other elements).
