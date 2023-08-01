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

After loading the package into the workspace:

```
]LoadPackages [tatin]PresentAPL
```

You can create a presentation with 

```
PresentAPL.MakePresentationFromFile <filename>
```

That works if you are happy with the defaults. If not you must create a parameter space, make your amendments and feed it to `MakePresentationFromFile` instead of a filename:


```
    parms←PresentAPL.CreateParms 
    parms.inputFilename←'/path/2/presentation.md'
    PresentAPL.MakePresentationFromFile parms                                        
```


## Meddy

Meddy is a basic Markdown editor that uses MarkAPL as converter. It can be used to edit Markdown that is supposed to be converted into a presentation.

See <https://github.com/aplteam/Meddy> for details.


## Misc

Please send comments, suggestions and bug reports to kai@aplteam.com.

License: http://creativecommons.org/licenses/LGPL/2.1/

A big thank you to:

* Stefan Goessner (<http://goessner.net/>) who created Slideous --- I stole a lot from it.
* Mike Mingard who created the theme PresentAPL_Green.css.

Kai Jaeger

Created: 2016-04-12

Last update: 2023-07-31

