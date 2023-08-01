[parm]: css    = 'PresentAPL_blue.css'

# Markdown & MarkAPL

[Data]:author="Kai Jaeger"
[Data]:company="APL Team Ltd"
[Data]:date="2016-03-10"

## Markdown & MarkAPL

### \{$author\}
### \{$company\}


## What is Markdown?
* Ordinary text
* Simple mark-up rules
* Readable and maintainable
* Markdown ==> valid HTML5

Note: it's a writing format rather than a publishing format.


## Markdown is useful for...  
* editing "ReadMe" files.
* editing pages for your web site.
* writing nicely formatted emails. 
* creating a presentation.
* writing an article for Vector.
* creating or maintaining content for MiServer.
* Writing a (cook) book ;)
* ...


## History, Specification
* 2004: John Gruber & Aaron Swartz
* From 2005 until 2011: chaos
* 2012: CommonMark <http://commonmark.org/>
* Internet media type text/markdown (IETF) underway
  
  As of March 2016: 
  
  * RFC 7763
  * RFC 7764
  
## Competitors?!
 * AsciiDoc
 * Texttile
 * Creole 
 * reStructuredText
 * AsciiDoc
 
 They all have their pros and cons...

 
## Is Markdowndown better than any of them?

**Definitely not!**

But: the war is over, and the winner is: Markdown!


## Big boys
* GitHub
* Stack Overflow
* SourceForge
* Open Streetmap
* Reddit
* Slack
* Trello
* Diaspora
* and many others


## Smaller boys
* Dyalog (MiServer)
* Dyalog user command ]adoc_browse
* APL wiki pages (one day)


## MarkAPL
* Dyalog class
* Markdown ==> HTML5
* Part of the APLTree project (totally free software)
* Available for download from <http://download.aplwiki.com>


## Why a Dyalog solution?
* Easier to integrate.
* We can add features as we please:
  * Table-of-contents
  * Function calls
  * Typographical sugar
  * Simplified bookmark links
  * Headers can be numbered
  * Defining data (key-value pairs) within Markdown
  * Use the lamp (`⍝`) for commenting out a line
 * There seems to be a converter available in any other programming language.

## Examples
* This slide show
* Launchy "readme" file
* Vector article
* ADOC


## Ideas

### HTML-to-Markdown converter

You don't want to convert your HTML files manually to Markdown, do you?

### Markdown-to-HTML converter

Having a class that does all the hard work is just the first step; an 
application is required that converts Markdown fils to HTML files:
 * Via the command line
 * Watching directories as a Windows Service or a daemon
 * Drag-and-drop onto the EXE file (Windows only)
 * Drag-and-drop onto the GUI (Windows only)
  
### Markdown editor
