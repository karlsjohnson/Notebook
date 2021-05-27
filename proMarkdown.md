# Markdown

## Headers

Add Headers to the Markdown file, add a `#` with a space at the beginning of a line.

``` md
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

## Emphasis

Emphasis, aka italics, with _asterisks_ or _underscores_.
Strong emphasis, aka bold, with **asterisks** or **underscores**.
Combined emphasis with **asterisks and _underscores_**.
Strike-through uses two tildes. ~~Scratch this.~~
Super and subscript: Text^super^, Text~sub~

## Lists

1. First ordered list item
2. Another item
3. Actual numbers don't matter, just that it's a number
4. And another item.

* Unordered list can use asterisks
* Or minuses
* Or pluses
  * Tab for sub lists

## Links

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com)

[I'm a reference-style link](https://www.mozilla.org)

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions](http://slashdot.org)

[Links to headers](#images)

Cross-References [link text](#myheaderid)

### Section header {# myheaderid .class}

Or leave it empty and use the [link text itself](http://www.reddit.com).

Some text to show that the reference links can follow later.

## Footnote

 footnote[^1](footnote)

## Images

Inline-style:
alt text

Reference-style:
alt text

## Code Highlighting

Inline `code` has `back-ticks around` it.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```javascript {.line-numbers}
function add(x, y) {
  return x + y
}
```

``` html
But let's throw in a <b>tag</b>.
```

## Tables

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- | ------------- | ----- |
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      | $12   |
| zebra stripes | are neat      | $1    |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

| Markdown | Less      | Pretty     |
| -------- | --------- | ---------- |
| _Still_  | `renders` | **nicely** |
| 1        | 2         | 3          |

## Block quotes

> Block quotes are very handy in email to emulate reply text.
> This line is part of the same quote.
Quote break.
> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can _put_ **Markdown** into a blockquote.

## Inline HTML

### Horizontal Rule

Three or more...

- - - -

Hyphens

- - - -

Asterisks

- - - -

Underscores

### Line Breaks

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a _separate paragraph_.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the _same paragraph_.

## YouTube Videos

[IMAGE ALT TEXT HERE](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

## MPE Extra Features

### Task lists

* [x] @mentions, refs, `[links]()`, **formatting**, and tags supported
* [x] list syntax required (any unordered or ordered list supported)
* [x] this is a complete item
* [ ] this is an incomplete item

### Emoji & FA

:smile:
:fa-car:
This only works for markdown-it parser but not pandoc parser.

### Definition Lists

Apple
: Pomaceous fruit of plants of the genus Malus in the family Rosaceae.
: An american computer company.

### Mathjax

**For inline formulas $...$**
text $\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$ text
**Block formulas, use $$...$$**
$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$

$x_i^2$ $\log_2 x$ text $\left(\frac{\sqrt x}{y^3}\right) ; \sqrt[3]{\frac xy} ; \sum_1^n$

### Symbols

* less than $\lt$
* greater than $\gt$
* less or equal $\le$
* greater or equal $\ge$
* not equal $\neq$
* times,divide, plus or minus, minus or plus  $\times \div \pm \mp$
* others $\approx \sim \simeq \cong \equiv \prec \cdots$
* $\cup$ $\cap \setminus \subset \subseteq$ $\supset$ $\in$ $\notin$ $\emptyset$
* spaces: $a,b$ for a thin space, $a;b$ for a wider space, $a\quad b$ and $a\qquad b$
* Accents and diacritical marks $$\hat x ; \widehat {xx-2}  ; \bar x  \overline x \vec x \overrightarrow x \overleftrightarrow x \dot x \ddot x$$
* Special characters $$ \backslash { } $ $$
* new line $$ fff \ ddd $$

### Import external files

@import "git.md"

**Supported files**!
.jpeg(.jpg), .gif, .png, .apng, .svg, .bmp, .csv, .mermaid

## Diagram

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
