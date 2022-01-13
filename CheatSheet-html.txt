# HTML

- Home page will always be 'index.html' 


- `! + tab`: shortcut to create a template

***

## Basic HTML Page Structure

> <!DOCTYPE html>
> <html>
>  <head>
>   <title>Document</title>
>   ............META, Links
>  </head>
>  <body>
>  .........Page Content
>  </body>
> </html>

1. `<!DOCTYPE html>`
- HTML Version

2. `<html></html>`
- Root element that will wrap all the elements in the page
- will always contain 1 HEAD element and 1 BODY element

3. `<head></head>`
- contains info about the page(meta, links, title)
- content within the HEAD element will not be visible on a page that is being rendered

 - Style element
   - define style information for a single HTML page
   - `<style></style>`
 - Meta element
   - meta data: will not be displayed on the page, but are used by browsers (how to display content or reload page), by search engines (keywords), and other web services. 
   - charset attribute: defines the character set used 
     - `<meta charset="UTF-8">`
   - name attribute: keywords for search engines
     - `<meta name="keywords" content="HTML, CSS, JavaScript">`
   - name attribute: description of webpage
     - `<meta name="description" content="Free Web tutorials">`
   - name attribute: author of a page
     - `<meta name="author" content="John Doe">`
   - name attribute: user's visible area of a web page.
     - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
   - http-equiv attribute: refresh document every 30 seconds
     - `<meta http-equiv="refresh" content="30">`
 - Link element
   - links to external resources (ie. css stylesheets & javascript file)
   - most often used to link to external style sheets
   - `<link rel="stylesheet" href="./styles.css">`
 - Title element
   - page title: defines the title of the document


4. `<body></body>`
- shows what will be displayed on the web page

***

### Semantic Markup
- not intended to affect the structure of the web but to add extra information to about the content between the opening and closing tags.
- semantic means _"relating to meaning"_

#### Why use Semantic HTML?
- for Accessibility. screen readers and browsers are able to interpret code better
- improves the website **SEO** (_Search Engine Optimization_)
- easy to understand source code

#### Semantic elements
- sup/sub element
  - `<sup></sup>` for superscript
  - `<sub></sub>` for subscript
  - can be inserted inline
- strong/em element
  - `<strong></strong>` gives strong importance to text
  - `<em></em>` gives emphasis to text
  - by default, browsers show this as bold and italic respectively.
- quotations
  - `<blockquote></blockquote>` for long quotations
  - `<q></q>` for short inline sentences
- abbreviations and acronyms
  - `title` attribute: specifies the full term
  - `<abbr title=""></abbr>`
- citations and definitions
  - `<cite></cite>` browsers render as italic
  - `<dfn></dfn>` some browser renders this as italic
- author details
  - `<address></address>` used to contain contact details of the author of the page. Often rendered as italic by browsers
- changes to content
  - `<ins></ins>` to insert a content
  - `<del></del>` to delete a content
  - `<s></s>` to strikethrough text
- header and nav
  - `<header></header>` is a container usually for either navigational links or intro content containing h1 to h6 headings
  - `<nav></nav>` is used to define a block of navigation links such as menus and tables of contents
    - can be used by itself or within the header tag
- main and footer
  - `<main></main>` used to encapsulate the dominant content within a webpage.
  - `<footer></footer>` the content at the bottom of the subject information
    - used to contain contact information and typically located at the bottom of the content
- section and article
  - `<section></section>` defines elements in a document, such as chapters, headings, or any other area of the document with the same theme.
  - `<article></article>` holds content that make sense on its own.
- aside
  - `<aside></aside>` used to mark additional info that can enhance another element but isn't required in order to understand the main content.
  - some common uses are: Bibliographies, endnotes, comments, pull quotes, editorial sidebars, additional info

Media Content
- audio
  - `<audio></audio>` used to embed audio content into a document.
  - `<source src="URL" type="audio/mp3"/>` to add a source for the audio and its type
    - this is placed within the opening and closing `audio` tag
    - `type` attribute: `audio/mp3` or `audio/mp4` what type of audio
  - `autoplay` attribute in opening tag: no value needed
  - `controls` attribute in opening tag: to add basic controls for the audio; no value needed
- video
  - `<video></video>` to add video content
  - `src` attribute is also needed within the opening tag
  - `loop` `autoplay` and `controls` attributes are also optional
  - text content by default is `Video not supported` if the browser is unable to play the video
- embed
  - `<embed />` can embed any media content including videos, audio files, and gifs from an external source.
- time
  - `<time></time>` represents either a time of day or a calendar date. 
  - `datetime` attribute: defines the machine-readable date with format: `year-month-date time-timezone`

***

### Special characters
- can be accessed and displayed by using `&`+`entity name`+`;`
- [list of entitiy names](https://www.tutorialspoint.com/html5/html5_entities.htm)

***

### Elements

Headings element
- `<h1></h1>` is used for the main headings
- `<h2></h2>` up to _h6_ are subheadings

***Note***: HTML is white space collapsing.
- html is going to ignore extra spaces
- ie. `<h3>hello             world</h3>` will return `hello world`

Dummy pick
- type  in `Lorem#` + `tab` where # states how many dummy words it will return

Image element
- is a self-closing element (without a closing tag)
- `img` + `tab` (default img element)
- `<img src="" alt="" />`
  - src and alt are ATTRIBUTES
  - ATTRIBUTES describes the element
    - `src` = source or location of the image
    - we need the *path* where the image is located. For _relative path_: 
      - type `/` if it is located in the same folder of the working file
      - type `./` which means it is in the same directory
      - type `../` if it is located in the actual folder just outside the directory
    - `alt` = alternate text that will be displayed if the src is not accessible or if the image is not located
    - `title` = provides additional info about the image. displays content when the user hovers over the image
    - For _absolute path_: just use its **URL**(_Uniform Resource Locator_).
--> just copy the image address of the photo from the web then paste it to the src attribute
- Getting COPYRIGHT-FREE images from the web:
  - [pixabay](https://pixabay.com/)
  - [pexels](https://www.pexels.com/) (also videos here)
  - [gratisography](https://gratisography.com/) (more on funny pictures)
- height/width attribute
  - to change the size of the image to be rendered
  - will adjust automatically both height and width if only width or height is entered
  - ***note:***
    1. For larger pictures, we can resize the image into smaller pixels for them to be rendered in the website faster.
    2. Use JPEG format if the picture has many different colors.
    3. Use GIF or PNG when saving images with few colors or large areas of the same color.
    4. Recommended resolution for web images is 72ppi (_pixels per inch_).
- Bitmap vs Vector images
  - Bitmap includes JPGs, GIFs, and PNGs.
    - they are made up of lots of miniature squares.
    - the __resolution__ of an image is the number of squares that fit within 1 by 1 inch square area.
    - computer screens are made of tiny squares called __pixels__. (_ppi_)
    - while print materials are made up of tiny circles called __dots__. (_dpi_)
  - Vector images are resolution-independent
    - are created by placing points on a grid and drawing lines between these points.
    - color can then be added to _fill in_ the lines that have been created.
    - __Scalable Vector Graphics__ (_SVG_) are used to directly display vector images on the web.
- Figure element
  - `<figure></figure>` contains images and their captions.
  - `<figcaption></figcaption>` contains the caption of images. placed within the `figure` element

Comments
- `<!--text-->`
- shorcut key: ctrl + `/`

Line break
- creates a new line
- `<br />`

Horizontal rules
- creates a break(_horizontal line_) between themes and/or sections
- `<hr />`

Bold and Italic
- `<b></b>` and `<i></i>`

Ordered list
- `<ol></ol>` displays numbered items
- `<li></li>` encloses each item in the list, also known as _list item_

Unordered List
- `<ul></ul>` displays bullets of list items
- `<li></li>` encloses each item in the list, also known as _list item_
- useful in navigation throughout the page
- can also display list of links within the page

Definition List
- `<dl></dl>` consist of a series of terms and their definitions
- `<dt></dt>` encloses each defined term
- `<dd></dd>` contains the definition

Links
- `<a href=""></a>` means _anchor_ element
  - `href` attribute: or _hypertext reference_ tells where the user is navigating to when clicking the link
  - `target` attribute: set to `_blank` so that when the clicking the link, it will open on another window or tab
  - `id` attribute: to navigate to certain portion of the page
    - `id="top"` will be referenced as `href="#top"`
- different objects other than text can also be inserted to be a link such as images, etc.
- can also use `#` if you don't know yet the link location or url instead of the URL itself --> dummy link
- email link
  - `<a href="mailto:myemail@gmail.com"></a>` use `mailto:` before your email address as the `href` value.

Table element
- `<table></table>` creates a table
- `<tr></tr>` defines the table row
- `<th></th>` defines the table headings
  - this adds title to rows and/or columns
  - `scope` attribute: takes in `row` or `col` value to specify if the heading belongs to a row or a column
- `<td></td>` defines the table data or cells of data
  - also the number of data defines how many column in a row
  - `colspan` attribute: accepts an integer (greater than or equal to 1) to denote the number of columns it spans across.
  - `rowspan` attribute: spans multiple rows
- `<tbody></tbody>` defines a table body to section off long tables
  - this includes all of the table's data excluding the _table headings_.
- `<thead></thead>` defines a table head to be sectioned off long tables
- `<tfoot></tfoot>` defines a table footer where the bottom part of the long table is sectioned off.

Setting up a FORM
- `<form action="" method=""></form>`
- used to collect data from a user
  - `action` attribute: where the information will be sent
  - `method` attribute: how the information will be processed
- most common type of form input is the __input__ element
  - `<input />` --> having different types (most common is text)
  - type in `input:text` you will get `<input type="text" name="" id="" />`
    - `name` attribute: only used when submitting data
    - `id` attribute: used for labeling
    - `placeholder` attribute: to show a preview text in the form
    - `value` element: used to hardcode data
      - _hardcode_ = fix in a text within the form

Submit element
  - type in `button:submit` you will get `<button type="submit"></button>`

Label element
  - `<label for=""></label>` where the value of the `for` attribute is the `id` attribute of the input element
  - clicking the label will highlight the id inserted in the for attribute

Textarea element
- `<textarea name="" id="" cols="30" rows="10"></textarea>`

Radio button
- `<input type="radio" name="" id="" value="" />`
  - `name` attribute: should always be the same in all related choices in a radio button so that only one choice can be picked
  - `value` attribute: the value that is passed on upon submitting

Checkbox button
- `<input type="checkbox" name="" id="">`
- can pick multiple choices

Select dropdownlist
- `<select name="language" id=""></select>`
- insert `<option></option>` within the select tag 

***

### VSCode extensions
Prettier - code formatter extension
  - go to settings and find the `editor.Format on save and Format on paste` option
  - check both options
  - it automatically formats the code upon saving/pasting

Live Server extension
- for real-time display of html coding
- click on `Go Live` in the taskbar to open in browser

Emmet extension
- built-in in the vs code editor
- ie. when you type `!` + `tab`
  - it will automatically create the default html Structure

Highlight Matching tag extension
- preferred values are:
  - `borderWidth: 3px, borderStyle: solid, borderColor: yellow`

Indent-rainbow extension
- install for colorful indentation


### Keyboard Shortcuts
- `ctrl` + `K`+ `S` (in vscode)

Multiple cursors
- `hold alt` + `click`

Select whole line
- triple click

Same Selection
- `ctrl` + `F2`

Start/end of Document
- `ctrl` + `home`/`end`

Navigate through words
- `ctrl` + `left`/`right`

Move whole line
- `alt` + `up`/`down`

Change tabs
- `alt` + `left`/`right`

Start a new line
- `shift` + `enter`


### External Resources
- [MDN](https://developer.mozilla.org/en-US/)
- [w3schools](https://www.w3schools.com/)


***

### Writing HTML with accessibility
1. It's important to define the natural language
   - do this via `lang` attribute
   - ie. `<html lang="en"></html>`

2. Hide content using `hidden` attribute
   - alternatively, you can use CSS `display: none` property

3. Sometimes it’s better to add a blank `alt` attribute to an `<img>` element
   - never omit the `alt` attribute but leave it empty even if the image is purely decorative

4. If you need a button, use the `<button>` element
   - use `button` element and not `div` even though its possible to use a `div` as a button
   - `button` element have more features like _focusable_, _clickable_(with mouse and keys), etc.

5. Structuring your markup correctly with headings is important
   - don't skip levels when nesting headings
   - don't use multiple `h1` headings

6. Using landmarks helps people navigate your site
   - proper sectioning of the webpage provide good landmarks for readers.
   - but don't overuse sectioning elements and use `div` elements if necessary especially for layout purposes while sections for semantics.

7. The main page content, header, and footer are also landmarks

8. Fieldsets are great for grouping form elements and giving them more context
   - `<fieldset></fieldset>` to group multiple radio buttons or checkboxes
   - add the object as a child of `<legend></legend>` element
   > ei. <form>
   >       <fieldset>
   >         <legend>T-Shirt size</legend>
   >         <input type="radio" id="s" name="shirtsize" />
   >         <label for="s">S</label>  
   >         <input type="radio" id="m" name="shirtsize" />
   >         <label for="m">M</label>  
   >         <input type="radio" id="l" name="shirtsize" />
   >         <label for="l">L</label>   
   >       </fieldset>
   >    </form>


--END OF DOC--



