[parm]:presentation = 1



# About PresentAPL

[Data]:author="Kai Jaeger"
[Data]:company=""
[Data]:date="2023-07-14"

## About PresentAPL

### \{$author\} \{$company\}
### \{$date\}


## PresentAPL

* **PresentAPL** is a Dyalog class
* It takes Markdown as input
* It uses MarkAPL to parse the Markdown
* It creates a slide show from the Markdown.
* It uses HTML5, CSS and a bit of JavaScript to achieve that
* All it needs is a modern browser

Use all MarkAPL features: paragraphs, lists, code blocks, tables, images, blockquotes, horizontal rulers, in-line markup (**bold**, _italic_, `APL code`, ~~deleted~~...) and more.



<div class="handout">


This is a paragraph **with** in-line mark-up that shows in print view only. The blank lines above and underneath this paragraph are essential. Only then are the two `<div>`s recognized as two rather than one HTML block, and only then is anything between the two `<div>`s interpreted as Markdown. 


</div>


## Advantages  

* Single stand-alone HTML file.
* Open Source.
* Simple and easy to use.

⍝ This file acts also as an example of how to create such a slide show.


## Disadvantages
* No animations other than animated GIFs & SVGs.


## Workflow

1. Create a presentation by editing a Markdown file. `AboutPresentAPL.md` is a starting point
1. Execute `]Tatin.LoadPackages [tatin]PresentAPL
2. Execute `PresentAPL.MakePresentationFromFile /path/2/markdown`
1. View the resulting HTML file - your presentation.


## Keyboard shortcuts

The following keys are used to control a PresentAPL presentation:{.nonincremental}

|``Key``       |``Comment``                                                       |
|--------------|------------------------------------------------------------------|
|`<PgDn>`      |Show the next slide                                               |
|`<PgUp>`      |Show previous slide                                               |
|`<Home>`      |First slide                                                       |
|`<End>`       |Last slide                                                        |
|`Cursor-right`|Show next item                                                    |
|`Cursor-left` |Hide current item                                                 |
|`M`           |Toggle mouse navigation (default=off)                             |
|`S`           |Toggle status bar visibility                                      |
|`P`           |For "Print": shows all slides at once including `<div>`s (handout)|

## Incremental

* All elements are shown incrementally.

  That means that by pressing `<CursorRight>` just one element at a time is revealed.
  
* If you don't want this just press `<PgDn>` - this shows a whole slide at once.
  
## Misc

I like to know when the last topic on a slide has been revealed. 

The bottom-left corner shows an arrow as long as not all items are revealed.



