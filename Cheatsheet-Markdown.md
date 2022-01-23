# Markdown (.md or .markdown files)

([see documentation here](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax))

([Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet))

([Markdown with Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown))

- a text-HTML conversion tool for web writers.
- plain-text formatting syntax.
- software tool.
- comprised of punctuation symbols.
- An alternative way to style a text document for readability and portability.
- needs a Markdown parser to render markdown in HTML.

---

## Headings

- use of `#` (hash)
- number of `#` corresponds to the heading level
  >ie. # Heading == Heading 1
- alternatively, first-level header can be produced through plain text with a row of equal(hyphen for second-level header) signs underneath

  ```markdown
  Syntax:

  Title of Document or Sub-Title of Document
  =================    ---------------------
  ```

## Emphasis

- italics: use `* *` or `_ _`
- bold: use `** **` or `__ __`
- strikethrough: use `~~ ~~`
- all bold and italic use `*** ***`

## Lists

### Unordered List

- use of `*`, `+` or `-` before the start of each item.

### Ordered List

- use of numbers followed by periods (ie. 1., 2. )

### Task List

- To create a task list, preface list items with a regular space character followed by `[ ]`. To mark a task as complete, use `[x]`.
- If a task list item description begins with a parenthesis, you'll need to escape it with `\`
  
  ```markdown
  Syntax: - [ ] \(Optional) Open a followup issue
  ```

## Quoting text

- use of `>` every start of a line
  
  ```markdown
  >quote 1
  >quote 2
  ```

## Quoting code

- use single pair  of backticks (\` \`) or press _ctrl_ + _e_ 
- The text within the backticks will not be formatted.
- To format code or text into its own distinct block (__code block__), use triple backticks.

  ```markdown
      ```specify coding language here(ie. git)
      git status
      git add
      git commit
      ```
  ```

## Links

- create an inline link by wrapping link text in brackets `[ ]` and then wrapping the URL in parentheses `( )`.
- You can also use the keyboard shortcut _command + k_ to create a link. When you have text selected, you can paste a URL from your clipboard to automatically create a link from the selection.
- Section links that directs you to a section by hovering over its heading to expose the link
- A relative link is a link that is relative to the current file.
  
  ```markdown
  Syntax: 
    [Contribution guidelines for this project](docs/CONTRIBUTING.md)
  ```

## Images

- You can display an image by adding `!` and wrapping the alt text in `[ ]`. Then wrap the link for the image in parentheses `()`.

  ```markdown
  ![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)
  ```

- You can specify the theme an image is displayed to by appending `#gh-dark-mode-only` or `#gh-light-mode-only` to the end of an image URL, in Markdown.

## Mentioning People and teams

- by using `@` followed by their username or team name.

## Using Emoji

- You can add emoji to your writing by typing `:EMOJICODE:`
- Typing `:` will bring up a list of suggested emoji.
- see the [Emoji-Cheat-Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

## Paragraphs

- You can create a new paragraph by leaving a blank line between lines of text.

## Footnotes

- You can add footnotes to your content by using this bracket syntax:
  
  ```markdown
  Here is a simple footnote[^1].
  
  A footnote can also have multiple lines[^2].  
  
  You can also use words, to fit your writing style more closely[^note].
  
  [^1]: My reference.
  [^2]: Every new line should be prefixed with 2 spaces.
    This allows you to have a footnote with multiple lines.

  [^note]: 
      Named footnotes will still render with numbers instead of the text but allow easier identification and linking.
      This footnote also has been made with a different syntax using 4 spaces for new lines.
  ```
- will render this:
  ![footnote example](https://docs.github.com/assets/cb-6345/images/site/rendered-footnote.png)

## Hiding content with Comment

- use this syntax:  `<!-- -->`

## Ignoring/Escaping markdown formatting

- use backslash `\` before the character you want to escape.
