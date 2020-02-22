---
title: Markdown Cheatsheet
---


This is intended as a quick reference and showcase. For more complete
info, see [John Gruber's original spec
](http://daringfireball.net/projects/markdown/).


##### Table of Contents

-   {{< iref "#headers" "Headers" >}}
-   {{< iref "#emphasis" "Emphasis" >}}
-   {{< iref "#lists" "Lists" >}}
-   {{< iref "#links" "Links" >}}
-   {{< iref "#attributes" "Attributes" >}}
-   {{< iref "#images" "Images" >}}
-   {{< iref "#code" "Code and Syntax Highlighting" >}}
-   {{< iref "#tables" "Tables" >}}
-   {{< iref "#blockquotes" "Blockquotes" >}}
-   {{< iref "#html" "Inline HTML" >}}
-   {{< iref "#hr" "Horizontal Rule" >}}
-   {{< iref "#lines" "Line Breaks" >}}
-   {{< iref "#videos" "Youtube videos" >}}


<a name="headers"/>
## Headers

```text
# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------
```

# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------


## Automatic TOC

The previous Table of Content is manual we just use:*

    :::text
    -   {{< iref "#headers" "Headers" >}}
    -   {{< iref "#emphasis" "Emphasis" >}}
    ...

We can also use an automatic table of content if the
[Table of Contents extension
](https://pythonhosted.org/Markdown/extensions/toc.html)
is enabled by including:

    [TOC]


<a name="emphasis"/>
## Emphasis

```text
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Some implementation uses two tildes for Strikethrough but not
python-markdown . ~~Scratch this.~~
```

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Some implementation uses two tildes for Strikethrough but not
python-markdown . ~~Scratch this.~~


<a name="lists"/>
## Lists

```text
1.  First ordered list item
2.  Another item
    *   Unordered sub-list.
1.  Actual numbers don't matter, just that it's a number
    1.  Ordered sub-list
4.  And another item.

    You can have properly indented paragraphs within list
    items. Notice the blank line above, and the leading spaces, for
    python-markdown you need to indent 4 spaces.

    This is a new paragraph.<br>
    Note that this line is separate, but within the same paragraph.

<br>

*   Unordered list can use asterisks
    *    sublist
-   Or minuses
+   Or pluses
```

1.  First ordered list item
2.  Another item
    *   Unordered sub-list.
1.  Actual numbers don't matter, just that it's a number
    1.  Ordered sub-list
4.  And another item.

    You can have properly indented paragraphs within list
    items. Notice the blank line above, and the leading spaces, for
    python-markdown you need to indent 4 spaces.

    This is a new paragraph.<br>
    Note that this line is separate, but within the same paragraph.

<br>

*   Unordered list can use asterisks
    *    sublist
-   Or minuses
+   Or pluses


To have a line break without a paragraph, you will need to use two
trailing spaces, or html &lt;br/&gt; in GFM or with
[python markdown nl2b
](https://pythonhosted.org/Markdown/extensions/nl2br.html)
trailing spaces are not required, ordinary newline break paragraphs,
and with pandoc you can also use a backslash followed by a newline.


If two lists are subsequent the second is considered as the
continuation of the first. To avoid it you can use a &lt;br/&gt;
&lt;-- comment--&gt; or &amp;nbsp;

### Definition Lists
The definitions lists are not part of
[Common Mark](http://spec.commonmark.org/), nor
[GFM](https://github.github.com/gfm/).

But we find
[Definition Lists extension
](https://pythonhosted.org/Markdown/extensions/definition_lists.html)
in the standard Python Markdown library, and also
[PHP markdown extra
](http://michelf.com/projects/php-markdown/extra/#def-list)
and numerous other formatters.

```text

Apple
:   Pomaceous fruit of plants of the genus Malus in
    the family Rosaceae.

Orange <a name="orange">
:   The fruit of an evergreen tree of the genus Citrus.

<dt id="distraction">Distraction</dt>
:   The fruit of lack of concentration.
```

Apple
:   Pomaceous fruit of plants of the genus Malus in
    the family Rosaceae.

Orange <a name="orange">
:   The fruit of an evergreen tree of the genus Citrus.

<dt id="distraction">Distraction</dt>
:   The fruit of lack of concentration.

As you see above we can add a {{< iref "#orange" "name" >}} or {{< iref "#distraction" "id" >}}
to have references to list items.

## Links {#links}

There are two ways to create links *inline* or *reference-style*.

```text
[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a link to a  relative path of a file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org  "The title is Slashdot!"
[link text itself]: http://www.reddit.com
```

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a link to a  relative path of a file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org  "The title is Slashdot!"
[link text itself]: http://www.reddit.com


Link targets i.e *id* or *name* can be defined either by giving the
html code:
```html
<a name="link-target">
{{< iref "#link" "Reference to the link target in the present page" >}}
```

<a name="link-target">
{{< iref "#link" "Reference to the link target in the present page" >}}

You can also use the title of sections *in lowercase, accent removed,  spaces
replaced by minus, and omitting special characters*.
```text
{{< iref "#inline" "link to the "Inline HTML" section" >}}
```

{{< iref "#inline" "link to the "Inline HTML" section" >}}

```text
You can also define id in attributes.
{: #attr-example .css-class }
```

You can also define id in attributes.
{: #attr-example .css-class }

It generates:
```html
<p class="css-class" id="attr-example">You can also define id in attributes.</p>
```

## Markdown parsers and attributes {#attributes}

The basis of defining a link target is in the {{< iref "#list" "previous section" >}}.

The general syntax for attributes is
```text
{: key1=val key2="long val" #myid .class1 .class2}
```

We have key-value pairs, `#myid` is equivlallent to `id=myid`,
`.class1` to `class=class1`,

An attribute list for a header is put on the line of the header.
for pandoc or php-markdown don't use `{: }` but `{ }`.


For a span level element you put it after the element. So:
```text
We are here inside the **second**{: #id1} paragraph.
{: #otherid}
```

generate:

```html
<p id="otherid">We are here inside the <strong id="id1">second</strong> paragraph.</p>
```

This work at least in python-markdown, maruku, and [kramdown
](https://kramdown.gettalong.org/syntax.html).

For pandoc you should use *native spans*.
```text
<span id=otherid>We are here inside the <span id=id1>**second**</span>
paragraph</span>
```


We take  a small example to show how attributes are handled
in diverse ways by the different parsers.

```text
Simple test
===========

## first section
We refer here to the {{< iref "#deux" "paragraph" >}} inside this
{{< iref "#sub_two" "subsection" >}}. Yes {{< iref "#otherid" "this one" >}}.

## second section
First an useless paragraph.
{: #python-markdown_style_ref class="red"}

### subparagraph of third paragraph {#sub_two class="blue"}
<div id="deux">
We are here inside the **second** paragraph.
<a id="otherid"></a>
</div>
```

With python markdown with _Extra_ extensions we get
```html
<h1 id="simple-test">Simple test</h1>
<h2 id="first-section">first section</h2>
<p>We refer here to the <a href="#deux">paragraph</a> inside this <a href="#sub_two">subsection</a>. Yes <a href="#otherid">this one</a>.</p>
<h2 id="second-section">second section</h2>
<p>First an useless paragraph. {: #python-markdown_style_ref class=&quot;red&quot;}</p>
<h3 id="sub_two" class="blue">subparagraph of third paragraph</h3>
<div id="deux">
<p>We are here inside the <strong>second</strong> paragraph. <a id="otherid"></a></p>
</div>
```

With pandoc
```html
<h1 id="simple-test">Simple test</h1>
<h2 id="first-section">first section</h2>
<p>We refer here to the <a href="#deux">paragraph</a> inside this <a href="#sub_two">subsection</a>. Yes <a href="#otherid">this one</a>.</p>
<h2 id="second-section">second section</h2>
<p>First an useless paragraph. {: #python-markdown_style_ref class=&quot;red&quot;}</p>
<h3 id="sub_two" class="blue">subparagraph of third paragraph</h3>
<div id="deux">
<p>We are here inside the <strong>second</strong> paragraph. <a id="otherid"></a></p>
```

The `{: }` is not understood.

With pandoc when disabling *raw_html*:
```html
<h1 id="simple-test">Simple test</h1>
<h2 id="first-section">first section</h2>
<p>We refer here to the <a href="#deux">paragraph</a> inside this <a href="#sub_two">subsection</a>. Yes <a href="#otherid">this one</a>.</p>
<h2 id="second-section">second section</h2>
<p>First an useless paragraph. {: #python-markdown_style_ref class=&quot;red&quot;}</p>
<h3 id="sub_two" class="blue">subparagraph of third paragraph</h3>
<div id="deux">
<p>We are here inside the <strong>second</strong> paragraph. &lt;a id=&quot;otherid&quot;&gt;&lt;/a&gt;</p>
</div>
```
The only attributes rendered are those in `<div>` and the `{ }`
syntax. It could seem strange that  `<div>` is handled even when
*raw_html* is disabled, but these `<div>` are not raw html for pandoc
but *native div*, in the same way there are *native span*.

This is quite important when converting to an other text format,
because if we use pandoc to convert this text to _asciidoc_ we get:

```text
Simple test
-----------

[[first-section]]
first section
~~~~~~~~~~~~~

We refer here to the link:#deux[paragraph] inside this
link:#sub_two[subsection]. Yes link:#otherid[this one].

[[second-section]]
second section
~~~~~~~~~~~~~~

First an useless paragraph. \{: #python-markdown_style_ref class="red"}

[[sub_two]]
subparagraph of third paragraph
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

[[deux]]
We are here inside the *second* paragraph.
```

The references in `<div>`, `<span>`, `{ }` are translated, the html
is not translated and appear as raw html.

## Images {#images}

```text
Here's our logo (hover to see the title text):

Inline-style:
![alt text](http://www.mzlinux.org/files/images/moon1.png "Logo Title Text 1")

Reference-style:
![alt text][logo]

[logo]: http://www.mzlinux.org/files/images/moon1.png "Logo Title Text 2"
```

Here's our logo (hover to see the title text):

Inline-style:
![alt text]( http://www.mzlinux.org/files/images/moon1.png "Logo Title Text 1")

Reference-style:
![alt text][logo]

[logo]:  http://www.mzlinux.org/files/images/moon1.png "Logo Title Text 2"

## Code and Syntax Highlighting {#code}

Inline `code` has `back-ticks around` it.

```text
Inline `code` has `back-ticks around` it.
```


Blocks of code are indented with four spaces.
In code blocks markup is uninterpreted.

    Simple Code block with
    uninterpreted _markup_


With the
[Fenced Code Blocks extension
](https://pythonhosted.org/Markdown/extensions/fenced_code_blocks.html)
code blocks can be fenced by lines with three
back-ticks <code>```</code>, or  three tilda <codde>~~~</code>.

Fenced Code Blocks are only supported at the document root level.
Therefore, they cannot be nested inside lists or blockquotes.

    ~~~~~~~~~~~~~~~~~~~~~~
    Fenced Code block with
    uninterpreted _markup_
    ~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~~~~~~~~
Fenced Code block with
uninterpreted _markup_
~~~~~~~~~~~~~~~~~~~~~~


Code blocks are part of the Markdown spec, but syntax highlighting
isn't. However, many renderers -- like Github's, _Stack Overflow_,
_Python-Markdown_, _Pandoc_, ...  -- support syntax
highlighting.

Which languages are supported and how those language
names should be written will vary from renderer to renderer. *Python
Markdown* uses [Pygments](http://pygments.org) supports highlighting
for dozens of language and markup; to see the complete list, see the
[Pygments language list](http://pygments.org/languages/) and
[Pygments lexers](http://pygments.org/docs/lexers/).

The name of the used lexer is either put at the end of the _fence
line_, or for an indented block in a header introduced by `:::`,
or inferred from the content of the block. Examples are given below.

    :::text
    ```javascript
    var s = "JavaScript syntax highlighting";
    alert(s);
    ```

        for (i=1; i<10; i++){
          print("The language is guessed by Pygment")
        }

    ~~~python
    s = "Python syntax highlighting"
    print s
    ~~~

        #!/bin/bash
        line="Bash syntax highlighting"
        echo ${line}


    ~~~console
    # echo "no more a comment"
    # line="sh script syntax highlighting"
    # echo ${line}
    ~~~

        :::text
        No syntax highlighting.
        But let's throw in a  <b>tag</b>.


```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

    for (i=1; i<10; i++){
      print("The language is guessed by Pygment")
    }

~~~python
s = "Python syntax highlighting"
print s
~~~

    #!/bin/bash
    # echo "just a comment"
    line="Bash syntax highlighting"
    echo ${line}

~~~console
# echo "no more a comment"
# line="sh script syntax highlighting"
# echo ${line}
~~~

    :::text
    No syntax highlighting.
    But let's throw in a  <b>tag</b>.



## Tables {#tables}

Tables aren't part of the core Markdown spec, but are one of
[GFM table](https://github.github.com/gfm/#tables-extension-).

{{< iref "php-markdown-extra" "PHP Markdown Extra" >}}
has a [table extension](https://michelf.ca/projects/php-markdown/extra/#table) similar
to the GFM one, but which does not allow column alignement. this syntax is used in
numerous formatters like {{< iref "markdown#hoedown" "Hoedown" >}},
{{< iref "markdown#lowdown" "lowdown" >}},
{{< iref "markdown#redcarpet" "Redcarpet" >}},
{{< iref "markdown#blackfriday" "BlackFriday"  >}}.
.

[Markdown Here](https://markdown-here.com/) a browser extension to
help you to write email supports them. They are an easy way of adding
tables to your email -- a task that would otherwise require
copy-pasting from another application.

In {{< iref "markdown#pandoc" "Pandoc" >}} there are many
[table extensions](https://pandoc.org/MANUAL.html#tables)
including these GFM tables under the extension name `pipe_table`.

Other GFM fully compatible formatters include
{{< iref "markdown#goldmark" "GoldMark" >}} _(GO)_ {{< iref "markdown#gfms" "gfms" >}}
_(Node.js)_.


```text
Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw
Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

Colons can be used to align columns.

| Tables        | Are           | Cool |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw
Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

## Blockquotes {#blockquotes}

```text
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.


## Inline HTML {#html}

You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

```text
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

## Horizontal Rule {#hr}

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

## Line Breaks {#lines}

A new paragraph is started by to consecutive new-lines.

To force a line return in the same paragraph, place two empty spaces
at the end of a line, as the line at end of file are often deleted by
the editor, or by _git_, it is more secure to use the html `<br/>`

```text
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This a separate paragraph,
and a continuation of the same line.<br>
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
```

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This a separate paragraph,
and a continuation of the same line.<br>
This line is only separated by a single newline, so it's a separate
line in the *same paragraph*.

## Youtube videos {#videos}

They can't be added directly but you can add an image with a link to
the video like this:

```text
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg"
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```

Or, in pure Markdown, but losing the image sizing and border:

```text
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
```

<!- taken from
https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet
with some modification from
https://github.com/dvidsilva/MarkdownReference/blob/master/README.md
-->
<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
