# ReadMe for PresentAPL


## Overview

`PresentAPL` is a package that allows you to convert a Markdown file into a presentation that can be viewed like a slide show with any modern browser by following some simple rules.

* For details regarding PresentAPL see the file ["About_PresentAPL.html"](http://htmlpreview.github.io/?https://github.com/aplteam/PresentAPL/blob/master/About_PresentAPL.html). (If you click on the link you will see the HTML file without the JavaScript being executed, which is a GitHub restriction. In order to view it as a presentation you need to download the file)


* The file ["Samples.html"](http://htmlpreview.github.com/?https://github.com/aplteam/PresentAPL/blob/master/Samples.html) acts as an example for a basic presentation. It can also be used as a starting point for your own presentation.

* The file ["MarkAPL_Cheatsheet.html"](http://htmlpreview.github.com/?https://github.com/aplteam/MarkAPL/blob/master/MarkAPL_CheatSheet.html) 
should get you going regarding Markdown and MarkAPL, the Markdown converter used by PresentAPL.

* The file ["MarkAPL.html"](http://htmlpreview.github.com/?https://github.com/aplteam/MarkAPL/blob/master/MarkAPL.html) 
is a full reference to MarkAPL.


## How to create a presentation  

Step 1: Load the package into the workspace:

```
]LoadPackages [tatin]PresentAPL
```

Step 2: Create a presentation from a file with:

```
    parms←PresentAPL.CreateParms 
    parms.inputFilename←'/path/2/presentation.md'
    PresentAPL.MakePresentationFromFile parms                                        
```

Note that you can also create a presentation from an array that holds markdown:

```
    parms←PresentAPL.CreateParms 
    parms.outputFilename←'/path/2/MyPresentation.html'
    myMD←'# My Markdown' '' 'A paragraph'
    PresentAPL.MakePresentationFromMarkdownArray myMD parms                                        
```


## Meddy

Meddy is a basic Markdown editor that uses MarkAPL as converter. It can be used to edit Markdown that is supposed to be converted into a presentation.

See <https://github.com/aplteam/Meddy> for details. Note however that Meddy is available only for the Windows platform.


## Misc

Please send comments, suggestions and bug reports to kai@aplteam.com.

License: http://creativecommons.org/licenses/LGPL/2.1/

A big thank you to:

* Stefan Goessner (<http://goessner.net/>) who created Slideous --- I stole a lot from it.

Kai Jaeger

Created: 2016-04-12

Last update: 2026-07-19


