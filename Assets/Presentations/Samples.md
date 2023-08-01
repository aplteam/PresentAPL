# Samples

[Data]:author="Kai Jaeger"
[Data]:company="APL Team Ltd"
[Data]:date="2016-03-10"

## Markdown Examples for Presentations

### \{$author\}, \{$company\}
### \{$date\}

## Headers

### Basic rules

* You must not use headers of level 1 - that level defines the name of the slide show.
* Headers of level 2 define a slide.

### Further levels

In any slide you may use headers of level 3, 4 5 and 6, although it is certainly a good idea to use not more than three levels.

## Paragraphs and in-line mark-up

Everything that is not identified as something else is a paragraph. The end of a paragraph is defined by an empty line or by starting a list.

### In-line mark-up

Examples for **bold**, _italic_ and **_bold and italic_** but also ~~deleted~~ and `APL code`. 

This is actually achieved by this:
 
~~~
Examples for **bold**, _italic_ and **_bold and italic_** 
but also ~~deleted~~ and ` APL code`.
~~~

You can insert line-breaks by either having a backslash (`\`) at the end of a line or having `<<br>>` anywhere in a paragraph, list item or table cell.  

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

You can have in-line code (sometimes referred to as verbatim) by<<br>>enclosing code within back-ticks: `{(+/⍵)÷⍴,⍵}`.

Code blocks are identified by fencing. You can use either `~` or ```` as fencing characters. You need at least three of them:

<pre>
~~~
{(+/⍵)÷⍴,⍵}
~~~
</pre>

results in this:

~~~
{(+/⍵)÷⍴,⍵}
~~~

You can also use `<pre>` and `</pre>` for defining a code block but there is not really any need for this.

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

![Pic](BlueDuck.jpg){style="height:250px; width:300px;"}


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

## Testing code -1-

Imagine you have this code block on a particular slide:

~~~
{{⍵/⍨2=+⌿0=⍵∘.|⍵}⍳⍵}20
~~~

You can insert this into that very slide:

~~~
[data]:exp1=2 3 5 7 11 13 17 19
~~~ 

## Testing code -2-

Imagine we have also a second code block with two lines:

~~~
 {+/⍵} 4 6
 {×/⍵} 2 3
~~~

For this we would define:

~~~
[data]:exp2=10 6
~~~

as the expected result.

## Testing code -3-

The `PresentAPL_Utils` namespace comes with a function `CheckSlide` which will check the results of all code blocks found on a sheet against the values it finds on `exp{n}`.

~~~
⍎⍎#.PresentAPL_Utils.CheckSlide 1⍎⍎
~~~

What's between the `⍎⍎` is the --- fully qualified --- name of a function. 

The function will get a namespace as right argument that contains all the data structures that define the current slide. The suggested name is `ns`.

The function can reference the injected data via `ns.data`. 

The `1` is passed as left argument and could refer to expression number 1.

## Testing code -4-

This is the check function:

~~~
    ∇ r←no CheckSlide ns;co;res;P;ex;b                                               
 [1]  P←##.PresentAPL                                                                
 [2]  co←P.GetCodeBlocks ns.html     ⍝ Code                                          
 [3]  res←{0::'' ⋄ ⍎¨⍵}¨co           ⍝ results                                       
 [4]  ex←2⊃¨ns.data                  ⍝ Expected                                      
 [5]  b←res≢¨{2=≡⍵:,⊂⍵ ⋄ ⍵}ex                                                        
 [6]  :If 1∊b                                                                        
 [7]      r←'Check code block(s): '                                                  
 [8]      r,←,↑{⍺,',',⍵}/↑¨b/ns.data                                                 
 [9]      r←'' '<p style="color:red;background-color:white;padding:3px;">'r'</p>' '' 
 [10]  :Else                                                                         
 [11]      r←''                                                                      
 [12]  :EndIf                                                                        
     ∇
~~~

## Testing code -5-

[data]:exp1=2 3 5 7 11 13 17 19
[data]:exp2=10 6

Let's use this in anger:

~~~
{{⍵/⍨2=+⌿0=⍵∘.|⍵}⍳⍵}100
~~~

The second block with two lines:

~~~
 {+/⍵} 4 6
 {×/⍵} 2 3
~~~

Note that in the first expression the right argument is 100 rather than 20. Therefore we won't get the expected result. Remember that we named the expected result for this `exp1`.

Here we would see the result of the check function, if any:

⍎⍎#.#.PresentAPL_Utils.CheckSlide⍎⍎


## Sophisticated stuff

PresentAPL offeres more. Essentially it offers almost anything the underlying Markdown parser, MarkAPL, has to offer.

For more information see the file MarkAPL.html which is a detailed reference of MarkAPL.