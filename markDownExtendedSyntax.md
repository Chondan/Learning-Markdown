# Extended Syntax

## Overview
The basic syntax outlined in John Gruber's original design document added many of the elements needed on a day-to-day basis, but it wasn't enough for some people. That's where extended syntax comes in.

Several individuals and organizations took it upon themselves to extend the basic syntax by adding additional elements like tables, code blocks, syntax hilighting, URL auto-linking, and footnotes. These elements can be enabled by using a lightweight markup language that builds upon the basic Markdown syntax, or by adding an extension to a compatible Markdown processor

---

## Availability 
Not all Markdown applications support extended syntax elements. You'll need to check whether or not the lightweight markup language your application is using supports the extended syntax elements you want to use. If it doesn't, it may still be possible to enable extensions in your Markdown processor.

### Lightweight Markup Languages
There are several lightweight makup languages that are supersets of Markdown. They include Gruber's basic syntax and build upon it by adding additional elements like tables, code blocks, syntax hilighting, URL auto-linking, and footnotes. Many of the most popular Markdown applications use one of the following lightweight markup
- CommonMark
- GitHub Flavored Markdown (GFM)
- Markdown Extra
- MultiMarkdown
- R Markdown

### Markdown Processors
There are dozens of Markdown processors available. Many of them allow you to add extensions that enable extended syntax elements. Check your processor's documentation for more information.

---

## Tables
To add a table, use three or more hyphens (---) to create each column's header, and use pipes (|) to separate each column. You can optionally add pips on either end of the table.

| Syntax | Description |
| --- | --- |
| Header | Title |
| Paragraph | Text |

> Tips: Creating tables with hyphens and pipes can be tedious. To speed up the process, try using the Markdown Tables Generator. Build a table using the graphical interface, and then copy the generated Markdown-formatted text into your file.

### Alignment
You can align text in the columns to the left, right or center by adding a colon (:) to the left, right, or both side of the hyphens withen the header row

| Align Left | Align Center | Align Right |
| :--- | :---: | ---: |
| text | text | text\| |

### Formatting Text in Tables
You can format the text within tables. For example, you can add links, code (words or phrases in backtick (`) only not code blocks), and emphasis

You can't add headings, blockquotes, lists, horizontal rules, images, or HTML tags.

### Escaping Pipe Characters in Tables
You can display a pipe (|) character in a table by using its HTML character code (&#124;).

---

## Fenced Code Blocks
The basic Markdown syntax allows you to create code blocks by indenting lines by four spaces or one tab. If you find that inconvenient, try using fenced code blocks. Depending on your Markdown processor or editor, you'll use three backticks(```) or three tildes (~~~) on the lines before and after the code block. The best part? You don't have to indent any lines!

```
{
    "firstName": "Chondan",
    "lastName": "Susuwan",
    "age": 22
}
```

~~~ javaScript
function() {
    greeting() {
        console.log("Hello world");
    }
}
~~~

### Syntax Highlighting
Many Markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color hilighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the backticks before the fenced code block.
```json
{
    "brand": "Aston Martin",
    "model": "DB11"
}
```

---

## Footnotes
Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets ([^1]). Identifiers can be numbers or words, but they can't contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself - in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text ([^1]: My footnote.) You don't have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

Here's a third note[^3].

[^3]: note

---

## Heading IDs
Many Markdown processors support custom IDs for headings - some Markdown processors antomatically add them. Adding custom IDs allow you to link directly to headings and modify them with CSS. To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading.

<h3 id="myheading">Example Linking Header</h3>
Go to me

### Linking to Heading IDs
You can link to headings with custom IDs in the file by creating a standard link with a number sign (#) followed by the custom heading ID.

[Heading IDs](#myheading)

---

## Definition Lists
Some Markdown processors allow you to create definition lists of terms and their corresponding definitions. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition

First Term
: This is the definition of the first term

<dl>
    <dt>First Term</dt>
    <dd>This is the definition of the first term.</dd>
</dl>

---

## Strikethrough
You can strikethrough words by putting a horizontal line through the center of them. The result looks ~~like this~~. This feature allows you to indicate that certain words are a mistake not mean for inclusion in the document. To strikethrough words, use two tilde symbols (~~) before and after the words.

~~The world is flat.~~ We know that the world is round.

---

## Task Lists
Task lists allow you to create a list of items with checkboxes. In Markdown applications that support task lists, checkboxes will be displayed next to the conten. To create a task list, add dashes (-) and brackets with a space ([ ]) in front of task list items. To select a checkbox, add an x in between the brackets ([x]).

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

---

## Emoji
There are two ways to add emoji to Markdown files: copy and paste the emoji into your Markdown-formatted text, or type emoji shortcodes.

### Copying and Pasting Emoji
In most cases, you can simply copy an emoji from a source like [Emojipedia](https://emojipedia.org) and paste it into your document. Many Markdown applications will automatically display the emoji in the Markdown-formatted text. The HTML and PDF files you export from your Markdown application should display the emoji.

> Tip: If you're using a static stie generator, make sure you encode HTML pages as UTF-8

### Using Emoji Shortcodes
Some Markdown applications allow you to insert emoji by typing emoji shortcodes. These begin and end with a colon and include the name of an emoji.

This is so funny! :joy:

---

## Automatic URL Linking
Many Markdown processors automatically turn URLs into links. That means if you type https://www.example.com, your Markdown processor will automatically turn it into a link even though you haven't used brackets.

---

## Disabling Automatic URL Linking
If you don't want a URL to bu automatically linked, you can remove the link by denoting the URL as code with backticks.
`https://www.example.com`

---

# END