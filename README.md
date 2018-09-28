# quickStart

## Lists

Unordered
* Item 1
* Item 2
  * Item 2a
  * Item 2b

Ordered
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

## Links
http://github.com - automatic!

[Link](http://github.com)

## Blockquotes

As Kanye West said:

> We're living the future so
> the present is our past.

## Inline code

I think you should use an `<addr>` element here instead

## Syntax highlighting
Here is an example of how you can use syntax highlighting with [Github Flavored Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/)

```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
You can also simply indicate your code by four spaces:

    function fancyAlert(arg) {
        if(arg) {
          $.facebox({div:'#foo'})
        }
    }

## Ignore Markdown formatting
You can tell GitHub to ignore (or escape) Markdown formatting by using `\` before the Markdown character.

Let's rename \*our-new-project\* to \*our-old-project\*.

## Tables
You can create tables by assembling a list of words and dividing them with hyphens `-`(for the first row) and then separating each column with a pipe `|`.

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

## Task Lists

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

If you include a task list in the first comment of an Issue, you will get a handy progress indicator in your issue list. It also works in Pull Requests!

Basic styles
------------

With this markup you can obtain *simple emhpasis* (usually rendered in italic text), **strong emphasis** (usually rendered in bold text), `source code` text (usually rendered in monospaced text), or ~~strikethrough~~ text (usually rendered with a line through text).

You may use also _this_ or __this__ notation to emphatize text, and you can use all them _**`together`**_ (and you can mix `*` and `_` )

If you look at the source code you may note that
even
if
you
break
the
lines,
the text is kept together
in a single paragraph

 Paragraphs are delimited by blank lines, leading and trailing spaces are removed

You may force a line break with two spaces
or with a `\`\
at the end of the line

Links
-----

- You can insert links in text like [this](/tutorial.md)

- You may add a [title](https://agea.github.io/tutorial.md "Markdown Tutorial") to your link (can you see the tooltip?)

- If your link contains spaces you have to write the [link](<http://example.com/a space>) between `<>`

- You can use spaces and markup inside the [link **text**](https://agea.github.io/tutorial.md)

- Long links may decrease source readability, so it's posible to define all links somewhere in the document (the end is a good place) and just reference the [link][tutorial.md], you may also collapse the reference if it matches the link text (example:  [tutorial.md][])

- You may also write directly the link: <https://agea.github.io/tutorial.md>

- It will work also for email addresses: <email@example.com> (you may write vaild email links also using [mailto](mailto:email@example.com) as protocol)


[tutorial.md]: https://agea.github.io/tutorial.md

Images
------

Syntax for images is like the syntax for links, but with a `!` before:

![alt text](img/1.png "image title")

![](img/2.png)

![ref]

[ref]: img/3.png

Lists
-----

To define a list of items, just put a `*`, a `-`, or a `+` at the start of the line of each item of the list followed by at least a space, to end the list, leave a blank line

* red
* green
* blue

- white
- grey
- black
+ yellow
+ pink
+ orange

You can also define numbered list, putting a number followed by a `.` or a `)` and a space at the start of the line (you may use any number, the first one is taken to start counting, then it will increment by one):

3.
2. you may leave blank items
1) or start
1) again

You can insert any block inside a list, you have to respect the indentation of the text of the list item

- A *paragraph* of text
  (spanning multiple lines),

  ```
  fenced code,
  ```

      indented code (4 spaces + 2 spaces for the list
      indentation, one blank line above, one below),

  > quotes,

  - another
    * list
      + (and so on...),

  - ### or headers

Headers
-------

There are two ways to define headers:

The biggest possible header
===========================

# You can also use this markup

(I prefer the first one as it's more readable when looking directly at the source code)

A sub heading
-------------

## This is the alternative format

### Then you can go smaller

#### And smaller

##### And even smaller

###### No, you can't go smaller than this

The good thing is that many tools that convert Markdown in HTML or PDF are able to generate the index of your document, or links to the headers automatically (like Github does on the [source](http://git.io/vfz98) of Markdown files)

Horizontal rules
----------------

You can use horizontal rules to separate paragraphs: you may use three or more `*`
******
or three or more `_` (you may insert spaces before, after or between the characters, no other charachters are allowed)
__ __ __ __ 

or three (or more) `-` 

---

but you have to be careful as it is similar to the header syntax, so if you write `---` immediatly after a single line of text you get an header, either you have to leave a blank line before the `---`, or you put it after multiple lines of text

HTML
----

Text between `<` and `>` that looks like an HTML tag is parsed as a raw HTML tag and will be rendered in HTML

While it may be useful when writing online content, please note that your tag may be stripped for security reasons and in output other than HTML you may have unexpected results

<p class="text-right">Look I'm right!</p>

This is the list of allowed html tags (case insensitive):

`article`, `header`, `aside`, `hgroup`, `blockquote`, `hr`, `iframe`, `body`, `li`, `map`, `button`, `object`, `canvas`, `ol`,`caption`, `output`, `col`, `p`, `colgroup`, `pre`, `dd`, `progress`, `div`, `section`, `dl`,`table`, `td`, `dt`, `tbody`, `embed`,`textarea`, `fieldset`, `tfoot`, `figcaption`, `th`, `figure`, `thead`, `footer`, `tr`, `form`, `ul`, `h1`, `h2`, `h3`, `h4`, `h5`, `h6`, `video`, `script`, `style`

Entities
--------

With the goal of making Markdown as HTML-agnostic as possible, all [valid HTML entities][] are recognized and converted into unicode characters

Named entities consist of `&` + any of the valid HTML5 entity names + `;`

Some examples:

- `&amp;` &amp;
- `&copy;` &copy;
- `&rarr;` &rarr;

[valid HTML entities]:(https://html.spec.whatwg.org/multipage/entities.json)

Escaping
--------

If you have to write something that would result in a Markdown vaild syntax, you can escape the first character of your expression (you may also escape any other punctuation character) with a `\`

\*not emphasized\*

\<br/> not a tag

\[not a link](/foo)

\`not code`

1\. not a list

\* not a list

\# not a header

\[foo]: /url "not a reference"

You may also escape the backslash itself \\*like this*
