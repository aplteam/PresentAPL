# Samples

[Data]:author="Kai Jaeger"
[Data]:company="APL Consultant"
[Data]:date="2026-07-13"

## Markdown Examples for Presentations

### \{$author\}

### \{$company\}

### \{$date\}

## Headers

### Basic rules

* The level-1 header defines the name of the slide show
* Level-2 headers define the slides

### Further levels

Feel free to use headers of level 3, 4, 5 and 6 in any slide.

## Paragraphs and in-line mark-up

Everything that is not identified as something else is a paragraph. The end of a paragraph is defined by an empty line or by starting a list.

### In-line mark-up

Examples for **bold**, _italic_ and **_bold and italic_** but also ~~deleted~~ and `APL code`. 

This is actually achieved by this:
 
~~~
Examples for **bold**, _italic_ and **_bold and italic_** 
but also ~~deleted~~ and `APL code`.
~~~

You can insert line-breaks by either having a backslash (`\`) at the end of a line or having `<br>` anywhere in a paragraph, list item or table cell.  

## Lists -1-

This is an example for a bulleted list:

~~~
* This
  * This -a-
  * This -b-
    
    Paragraph belonging to "This -b-"
* That
~~~

* This
  * This -a-
  * This -b- is a paragraph
    
    Paragraph belonging to "This -b-"
* That

## Lists -2-

This is an example for an ordered list:

~~~
2. First
2. Second
~~~

2. First
2. Second  

Note that the first number used in a numbered list defines the start of the list.

From then on any digit will do.

## Code

You can have in-line code (sometimes referred to as verbatim) by<br>enclosing code within back-ticks: `{(+/⍵)÷⍴,⍵}`.

Code blocks are identified by fencing. You can use either `~` or ` as fencing characters. You need at least three of them:

<pre>
~~~
{(+/⍵)÷⍴,⍵}
~~~
</pre>

results in this:

~~~
{(+/⍵)÷⍴,⍵}
~~~

You can also use `<pre>` and `</pre>` for defining a code block, but there is not really any need for this.

## Images -1-

Images can be included anywhere:

~~~
![Alt Text](/url "My title")
~~~

The URL is mandatory.

Both the Alt Text as well as the Title are optional, so this would work as well:

~~~
![](/url)
~~~ 

## Images -2-

By default images are shown left-aligned with their "natural" size.

With "special attributes" you can change this: 

~~~
![Pic](/url){style="height:250px; width:300px;"}
~~~


## Tables -1-

Simplest possible table:

~~~
APL |
JavaScript |
~~~

APL |
JavaScript |


## Tables -2-

No column headers but column alignment:

~~~
|:-----|:------:|
|John Doe   | Great entertainer |
| Tim Smith | Boring |
~~~

|:-----|:------:|
|John Doe   | Great entertainer |
| Tim Smith | Boring |


## Tables -3-

Tables with headers and column alignment: 

~~~
| Name        | Age  | Comment           |
|:------------|-----:|:-----------------:|
|John Doe     | 28   | Great entertainer |
| Tim Smith   | 54   | Boring            |
| Don Miller  | 23   | Witty             |
| Nils Meyer  | 32   | Well...           |
~~~

| Name        | Age | Comment |
|:------------|-----:|:-----------:|
| John Doe    | 28   | Great entertainer |
| Tim Smith   | 54   | Boring |
| Don Miller  | 23   | Witty |
| Nils Meyer  | 32   | Well... |

## Blockquotes

Blockquotes use the same mark-up as emails: just put a `<` followed by a blank and the paragraph --- or whatever else is going to be part of the blockquote --- will be marked up as such:

> APL is a mistake, carried through to perfection. (Edsger Dijkstra)

> You probably know that arrogance in computer science is measured in nano-Dijkstras. (Alan Kay)   

## Horizontal rulers

This (note the essential blank line) :

~~~

---
~~~

results in this:

--- 

## Sophisticated stuff

PresentAPL offeres more. Essentially it offers almost anything the underlying Markdown parser, MarkAPL, has to offer.

For more information see <https://github.com/aplteam/MarkAPL>










