# Learning Markdown
## Overview
Nearly all Markdown applications support the basic syntax outlined in John Gruber's original design document. There are minor variations and discrepacies between Markdown processors - those are noted inline wherever possible

---

## Heading
To create a heading, add number sign(#) in front of a word or phrase. The number signs you use should correspond to the heading level. For example, to create a heading level three (\<h3>), use three number signs (e.g., ### My Header).
### Header level3
#### Header level4
##### Header level5
###### Header level6

### Alternative Syntax
Alternatively, on the line below the text, add any number of == characters for heading level 1 or -- character for heading level 2.

Heading level 1
===============

Heading level 2
---------------

### Heading Best Practices
Markdown applications don't agree on how to handle a missing space between the number signs(#) and the heading name. For compatibility, always put a space between the number signs and the heading name.

---

## Paragraphs
To create paragraphs, use a blank line to separate one or more lines of text

I really like using Markdown

I think I'll use it to format all of my documents from now on.
### Paragraph Best Practices
Unless the paragraph is in a list, don't indent paragraphs with spaces or tabs

Don't put tabs or spaces in front of your paragraphs.

Keep lines left-aligned like this.

---

## Line Breaks
To create a line break (<br>), end a line with two or more spaces, and then type return.

This is the first line.
And this is the second line.
### Line Break Best Practices
You can use two or more spaces (commonly referred to as "trailing whitespace") for line breaks in nearly every Markdown application, but it's controversial. It's hard to see trailing whitespace in an editor, and many people accidentally or intentionally put two spaces after every sentence. For this reason, you may want to use something other than trailing whitespace for line breaks. Fortunately, there is another option supported by nearly every Markdown application:the <br> HTML tag.

For compatibility, use trailing white space or the <br> HTML tag at the end of the line.

There are two other options I don't recommend using. CommonMark and a few other lightweight markup languages let you type a backslash at the end of the line, but not all Markdown applications support this. so it isn't a great option from a compatibility perspective. And at least a couple lightweight markup languages don't require anything at the end of the line - just type return and they'll create a line break.

---

## Emphasis
You can add emphasis by making text bold or italic.
### Bold
To bold text, add two asterisks or underscores before and after a word or phrase. To bold the middle of a word for emphasis, add two asterisks without spaces around the letters

I just love **bold text**.
I just love __bold text__
Love **is** bold
#### Bold Best Practices
Markdown applications don't agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold the middle of a word for emphasis.

Don't do this -> Love__is__bold
Do this -> Love **is** bold

### Italic
To italicize text, add one asterisk or underscore before and after a word or phrase. To italicize the middle of a word for emphasis, add one asterisk without spaces around the letters.

Italicize text is the *cat's meow*.
Italicize text is the _cat's meow_.
A *cat* meow.
#### Italic Best Practices
Markdown applications don't agree on how to handle underscores in the middle of a word. For compatilbility, use asterisks to italicize the middle of a word for emphasis.

Do this -> A *cat* meow.
Don't do this -> A_cat_meow.
### Bold and Italic
To emphasize text with bold and italics at the same time, add three asterisks or underscores before and after a word or phrase. To bold and italicize the middle of a word for emphasis, add three asterisks without spaces around the letters.

This text is ***really important***.
This text is ___really important___.
This text is __*really important*__.
This text is **_really important_**.
This is really***very***important text.
#### Bold and Italic Best Practices
Markdown applications don't agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold and italicize the middle of a word for emphasis.

Do this -> This is really***very***important text.
Dont' do this -> This is really___very___important text.

---

## Blockquotes
To create a blockquote, add a > in front of a paragraph.

> Dorothy followed her through many of the beautiful rooms in her castel.
### Blockquotes with Multiple Paragraphs
Blockquotes can contain multiple paragraphs. Add a > on the blank lines between the paragraphs.

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

#### Nested Blockquotes
Blockquotes can be nested. Add a >> in front of the paragraph you want to nest.

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

#### Bloackquotes with Other Elements
Blockquotes can contain other Markdown formatted elements. Not all elements can be used - you'll need to experiment to see which ones work.

> The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
> *Everything* is going according to **plan**.

---

## Lists
You can organize items into ordered and unordered lists.

### Ordered Lists
To create an ordered list, add line items with numbers followed by periods. The numbers don't have to be in numerical order, but the list should start with the number one.

##### First List
1. First item
2. Second item
    1. Indented item
    2. Indened item
3. Third item
##### Second List
1. First item
1. Second item
1. Third item

#### Ordered List Best Practice
CommonMark and a few other lightweight markup languages let you use a paranthesis()) as a delimiter (e.g., 1) First item), but not all Markdown applications support this, so it isn't a great option from a compatibility perspective. For compatibility, use periods only.

Do this
1. First item
2. Second item

Don't do this
1) First item
2) Second item

### Unordered Lists
To create an unordered list, add dashes (-), asterisks (*), or plus signs (+) in front of line items. Indent one or more items to create a nested list.
First list
- First item
- Second item
- Third item

Second list
* First item
* Second item
    - Indented item
        - Indented item
* Third item

Third list
+ First item
+ Second item
+ Third item

#### Unordered List Best Practices
Markdown applications don't agree on how to handle different delimiters in the same list. For compatilbility, don't mix and match delimiters in the same list - pick one and stick with it.

Do this
- First item
- Second item

Don't do this
- First item
* Second item

#### Adding Elements in Lists
To add another element in a list while perserving the continuity of the list, indent the element four spaces or one tab, as shown in the following examples.

* This is the first list item.
* Here's the second list item.
    I need to add another paragraph below the second list item.
* And here's the third list item.

#### Blockquotes
* This is the first list item.
* Here's the second list item.
    > A blockquote would look great below the second list item.
* And here's the third list item.

#### Code Blocks
Code blocks are normally indented four spaces or one tab. When they're in a list, indent them eight spaces or two tabs.

For example
1. Open the file.
2. Find the following code block on line 21:

        <html>
            <head>
                <title>Test</title>
            </head>
1. Update the title to match the name of your website.

#### Images
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.
    ![Coala](https://upload.wikimedia.org/wikipedia/commons/4/49/Koala_climbing_tree.jpg)
3. Close the file.

#### Lists
You can nest an unordered list in an ordered list, or vice versa.
1. First item
2. Second item
    - Indented item

- First item
- Second item
    1. Indented item

---

## Code
To denote a word or phrase as code, enclose it in backtick(`).

At the command prompt, type `nano`.

### Escaping Backticks
If the word or phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks(``).

``Use `code` in your Markdown file.``

### Code Blocks
To creat code blocks, indent every line of the block by at least four spaces or one tab.

    <html>
        <head></head>
    </html>
    
---

## Horizontal Rules
To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves.

### Horizontal Rule Best Practices
For compatibility, put blank lines before and after horizontal rules.

---

## Links
To create a link, enclose the link text in brackets (e.g., [Duck Duck Go]) and then follow it immediately with the URL in parenthesis (e.g., (https://duckduckgo.com)).

> My favorite search engine is [Google](https://www.google.com)
> My favorite social media platform is [facebook].

[facebook]: <https://www.facebook.com>

### Adding Titles
You can optionally add a title for a link. This will appear as a tooltip when the use hovers over the link. To add a title, enclose it in parentheses after the URL

> My favorite search engine is [Google](https://www.google.com "Go to google")

### URLs and Email Address
To quickly turn a URL or email address into a link, enclose it in angle brackets.

<https://www.markdownguide.org>
<fake@example.com>

### Formatting Links
To emphasize links, add asterisks before and after the brackets and parentheses. To denote links as code, add backticks in the brackets.

I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).

### Referece-style Links
Reference-style links are a special kind of link that make URLs easier to display and read in Markdown. Reference-style links are constructed in two parts: the part you keep inline with your text and the part you store somewhere else in the file to keep the text easy to read.

#### Formatting the First Part of the Link
The first part of a referece-style link is formatted with two sets of brackets. The first set of brackets surrounds the text that should appear linked. The second set of brackets displays a label used to point to the link you're storing eleswhere in your document

Although not required, you can include a space between the first and second set of brackets. The label in the second set of brackets is not case sensitive and can include letters, numbers, spaces, or punctuation.

This means the following example formats are roughly equivalent for the first part of the link:
- [Google][1]
- [Google][2]
- [Google][3]
- [twitter]

#### Formatting the Second Part of the Link
The second part of a reference-style link is formatted with the following attributes:
1. The label, in brackets, followed immediately by a colon and at least one space (e.g., [label]: ).
2. The URL for the link, which you can optionally enclose in angle brackets.
3. The optional title for the link, which you can enclose in double quotes, single quotes, or parentheses.

This means the following example formats are all roughly equvilent for the second part of the link:

[1]: https://www.google.com
[2]: https://www.google.com "Go to google"
[3]: https://www.google.com (Go to google)
[twitter]: <https://www.facebook.com> "Go to twitter"

### Link Best Practices
Markdown applications don't agree on how to handle spaces in the middle of a URL. For compatibility, try to URL encode any spaces with %20.

Do this -> [link](https://www.google.com?q=machine%20learning)

Don't do this -> [link](https://www.google.com?q=machine learning)

---

## Images
To add an image, add an exclamatino mark (!), followed by alt text in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title after the URL in the parentheses.

Coala Image
![Coala](https://upload.wikimedia.org/wikipedia/commons/4/49/Koala_climbing_tree.jpg "Coala Image")

### Linking Images
To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parenthesis.
[![Coala](https://upload.wikimedia.org/wikipedia/commons/4/49/Koala_climbing_tree.jpg "Coala Image")](https://www.google.com "Search more on gogle")

---

## Escaping Characters
To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash (\\) in front of the character.

\* Without the backslash, this would be a bullet in an unordered list.

---

## HTML
Many Markdown applications allow you to use HTML tags in Markdown-formatted text. This is helpful if you prefer certain HTML tags to Markdown syntax. For example, some people find it easier to use HTML tags for images. Using HTML is also helpful when you need to change the attributes of an element, like specifying the color of text or changing the width of an image.

This **word** is bold. This <em>word</em> is italic.

### HTML Best Practices 
For security reasons, not all Markdown application support HTML in Markdown documents. When in doubt, check your Markdown application's documentation. Some applications support only a subset of HTML tags.

---


















# END