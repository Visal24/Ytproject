<img src="img/markdown-mark-white.svg" weight="100px" height="100px">

# Basic Syntax
The Markdown elements outlined in the original design document.

### Overview[^1]
Nearly all Markdown applications support the basic syntax outlined in the original Markdown design document. There are minor variations and discrepancies between Markdown processors — those are noted inline wherever possible.

### Headings[^2]
|**Markdown**| **HTML**| **Rendered Output**|
|------------|---------|--------------------|
|# Heading<br> Level 1|`<h1>Heading level 1</h1>`>| <h1>Heading level 1</h1>|
|## Heading<br> Level 2|`<h2>Heading level 2</h2>`>| <h2>Heading level 2</h2>|
|### Heading<br> Level 3|`<h3>Heading level 3</h3>`>| <h3>Heading level 3</h3>|
#### Alternate Syntax
|**Markdown**| **HTML**| **Rendered Output**|
|------------|---------|--------------------|
|Heading Level 1<br>=============|`<h1>Heading level 1</h1`>| <h1>Heading level 1</h1>|
|Heading Level 2<br>---------------------- |`<h2>Heading level 2</h2`>| <h2>Heading level 2</h2>|

### Paragraphs[^3]

|**Markdown**| **HTML**| **Rendered Output**|
|------------|---------|--------------------|
|The paragraphs are waiting at the whole of content <br><br> The content are very useful|`<p>The paragraphs are waiting at the whole of content</p> <p>The content are very useful</p>`>| <p>The paragraphs are waiting at the whole of content</p> <p>The content are very useful</p>|

### Emphasis[^4]

|**Markdown**| **HTML**| **Rendered Output**|
|------------|---------|--------------------|
|`**Bold**` text appeared or<br> `__ Bold __`|`<strong>Bold</strong>` text appeared| <strong>Bold</strong> text appeared|
`*Italic*` text appeared or<br> `_ Italic _`|`<em>Italic</em>` text appeared| <em>Italic</em> text appeared|
|***Bold and Italic*** text appeared or<br> `***Bold and Italic***` or `**_` or `___` or `__*`|`<em><strong>Bold and Italic</strong></em>` text appeared|<em><strong>Bold and Italic</strong></em> text appeared

### BLockquotes[^5]

    > The tails of a man who survive every condition
    > > Begin the story
    > > How to survive
    > > > In the forest
    > > > Among many people

Output:
> The tails of a man who survive every condition
    > > Begin the story
    > > How to survive
    > > > In the forest
    > > > Among many people

### Lists[^6]
|**Markdown**| **HTML**| **Rendered Output**|
|------------|---------|--------------------|
|1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item|`<ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>`|<ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>|
|1. First item<br>1. Second item<br>1. Third item<br>1. Fourth item|`<ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>`|<ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>|
|1. First item<br>5. Second item<br>3. Third item<br>2. Fourth item|`<ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>`|<ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>|
|1. First item<br>2. Second item<br>3. Third item<br>&nbsp; &nbsp;1. Indented item<br> &nbsp; &nbsp;  2. Indented item<br>4. Fourth item|`<ol><li>First item</li><li>Second item</li><li>Third item<ol><li>Indented item</li><li>Indented item</li></ol></li><li>Fourth item</li></ol>`|<ol><li>First item</li><li>Second item</li><li>Third item<ol><li>Indented item</li><li>Indented item</li></ol></li><li>Fourth item</li></ol>|
### Code [^7]
    ``Use `code` in your Markdown file.``

Output:
``Use `code` in your Markdown file.``
#### Code Blocks[^7]
To create code blocks, indent every line of the block by at least four spaces or one tab.

        <html>
            <head>
            </head>
        </html>
Output:

    <html>
        <head>
        </head>
    </html>

### Horizontal Rules [^8]
    Try to put a blank line before...

    ---
    ***
    ___

    ...and after a horizontal rule.
Output:

Try to put a blank line before...

---
***
___

...and after a horizontal rule.

### Links[^9]
    My favorite search engine is [Duck Duck Go](https://duckduckgo.com)
Output:
My favorite search engine is [Duck Duck Go](https://duckduckgo.com)
#### Adding Title[^9]
    My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
Output:
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

#### URLs and Email Addresses[^9]
    I love supporting the **[EFF](https://eff.org)**.
    This is the *[Markdown Guide](https://www.markdownguide.org)*.
    See the section on [`code`](#code).
Output:
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
#### Reference-style Links[^9]
Reference-style links are a special kind of link that make URLs easier to display and read in Markdown. Reference-style links are constructed in two parts: the part you keep inline with your text and the part you store somewhere else in the file to keep the text easy to read.
#### Formatting of the Link[^9]
1st Part
- [hobbit-hole][1]
- [hobbit-hole][1]
  
2nd Part
`
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)
`
### Images[^10]
`![The San Juan Mountains are beautiful!](img/san-juan-mountains.avif "San Juan Mountains")`
Output:

![The San Juan Mountains are beautiful!](img/san-juan-mountains.avif "San Juan Mountains")

Linking Images
[![An old rock in the desert](img/shiprock.avif "Ship rock")](https://mdg.imgix.net/assets/images/shiprock.jpg?auto=format&fit=clip&q=40&w=1080)

### HTML[^12]
For security reasons, not all Markdown applications support HTML in Markdown documents. When in doubt, check your Markdown application’s documentation. Some applications support only a subset of HTML tags.

Use blank lines to separate block-level HTML elements like `<div>, <table>, <pre>, and <p>` from the surrounding content. Try not to indent the tags with tabs or spaces — that can interfere with the formatting.

You can’t use Markdown syntax inside block-level HTML tags. For example,` <p>italic and **bold**</p>` won’t work.



[^1]: Overview
[^2]: Heading
[^3]: Paragraphs
[^4]: Emphasis
[^5]: BLockquotes
[^6]: Lists
[^7]: Code
[^8]: Horizontal Rules
[^9]: Links
[^10]:Images
[^11]: Escaping Characters
[^12]: HTML

