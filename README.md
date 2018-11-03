# ReadMe for PresentAPL


## Overview

`PresentAPL.exe` is a program that allows you to convert a Markdown file into a presentation that can be viewed like a slide show with any modern browser by following some simple rules.

* For details regarding PresentAPL see the file ["About_PresentAPL.html"](http://htmlpreview.github.com/?https://github.com/aplteam/PresentAPL/blob/master/About_PresentAPL.html).


* The file `Samples.html` acts as an example for a basic presentation. It can also be used as a starting point for your own presentation.

* The file `MarkAPL_Cheatsheet.html` should get you going regarding Markdown and MarkAPL, the Markdown converter used by PresentAPL.

* The file `MarkAPL.html` is a full reference to MarkAPL.


## How to create a presentation  

### Drag and drop

The simplest way to use PresentAPL is to drag and drop one or more presentation files (`*.md`) onto `PresentAPL.exe`.

### Command line

Call `PresentAPL.exe` --- for example in a console window --- and pass the name(s) of the markdown files (extension `.md` is required!) you want to be converted into presentations.

### Via the context menu

You can also add a context menu entry "Create presentation with PresentAPL"; see below for details how to do that.

The resulting presentation is in any case a stand-alone HTML file created from the markdown file. If there is already a file with that name it will be overwritten. It will go into the same folder the source files came from, and with the same name except the extension which will be `.html`.


## How to change parameters

If you want to change default parameters then you have several choices:

* Change the name of the file `PresentAPL.ini.RemoveMe` to `PresentAPL.ini` and make adjustments to the file. Naturally the file must be a sibling of the EXE. 

  This is the recommended way for changing a parameter for **all** your presentations.
  
* Embed your parameters into your Markdown file. This is an example:

  ~~~
  standalone = 0
  ~~~
  
  This is the recommended way to change a parameter for just that presentation.
 
* Load the workspace PresentAPL.dws into Dyalog 15.0 Unicode or better.

  The function `#.PresentAPL_Utils.RecreatePresentAPLsPresentations` gives you examples of how to...

  * create a parameter namespace.
  * set some parameters.
  * create a presentation.


## Using PresentAPL from within APL code

You can also use the class `PresentAPL` from within your Dyalog APL workspace. It needs the class `MarkAPL` and the namespace script `APLTreeUtils`. For details see the class `PresentAPL`. 


## Add a command "Create presentation with PresentAPL" to context menu.

You can quite easily add such a context menu command so that whenever you right-click on a file with the extension `.md` or `.markdown` it will make an appearance.

That would have the same effect as drag-and-drop but is certainly more convenient.

To make the context command available first check and amend the file `MarkdownFile.reg`. When done just double-click the file and it will be imported into your Windows Registry. You will need admin rights for this. The new (additional) context menu command will be available straight away.

When the command is issued on a Markdown file PresentAPL will create a presentation from that Markdown file and save it as a sibling of the Markdown file.

## Meddy

Meddy is a basic Markdown editor that uses MarkAPL as converter. It can be used to edit Markdown that is supposed to be converted into a presentation.

See <https://github.com/aplteam/Meddy> for details.


## Misc

Please send comments, suggestions and bug reports to kai@aplteam.com.

License: http://creativecommons.org/licenses/LGPL/2.1/

A big thank you to:

* Stefan Goessner (<http://goessner.net/>) who created Slideous --- I stole a lot from it.
* Mike Mingard who created the theme PresentAPL_Green.css.

Kai Jaeger ⋄ APL Team Ltd

Created: 2016-04-12

Last update: 2018-10-12
