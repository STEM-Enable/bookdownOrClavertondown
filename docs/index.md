---
title: "RMarkdown, Bookdown or ClavertonDown?"
author: 'Emma Cliffe, Skills Centre: MASH'
site: bookdown::bookdown_site
language: en
documentclass: article
classoption: a4paper
fontsize: 10pt
geometry: margin=2.5cm
output:
  clavertondown::gitbook_clav:
    split_by: section
    keep_md: true
    config:
      download: [["Notes.html", "HTML page"], ["Notes.pdf","Standard print PDF"], ["NotesClear.pdf","Clear print PDF"], ["NotesLarge.pdf","Large print PDF"], ["Notes.docx","Accessible Word document"], ["Notes.epub","Accessible EPub book" ]]
      sharing: no
    pandoc_args: --default-image-extension=svg
  clavertondown::pdf_clav:
    latex_engine: pdflatex
    keep_tex: true
    fig_caption: true
    toc: true
    extra_dependencies: ["float"]
    pandoc_args: --default-image-extension=pdf
  clavertondown::epub_clav:
    toc: false
    pandoc_args: --default-image-extension=svg
  clavertondown::html_clav:
    toc: true
    pandoc_args: --default-image-extension=svg
  clavertondown::word_clav:
    toc: true
    number_sections: true
    keep_md: true
    pandoc_args: --default-image-extension=svg
linkcolor: blue
header-includes:
  - \newcommand{\BOO}{BOO}
---

\newpage
\pagenumbering{arabic}

# An introduction {-}

* Requirements
* Formats and transforms
* Markdown
* RMarkdown
* Bookdown
* Clavertondown

# Requirements

* Public Sector Bodies (Websites and Mobile Applications) (No. 2) Accessibility Regulations requires at least one of:
  * [Web: WCAG 2.1 AA](https://accessibilityinsights.io/docs/en/web/overview) +  [MathJax!](https://docs.mathjax.org/en/v2.7-latest/misc/accessibility-features.html)
  * [Word 365: Accessibility checker + Equation editor](https://support.office.com/en-gb/article/make-your-word-documents-accessible-to-people-with-disabilities-d9bf3683-87ac-47ea-b91a-78dcacb3c66d)
  * [PowerPoint 365: Accessibility checker + Equation editor](https://support.microsoft.com/en-us/office/make-your-powerpoint-presentations-accessible-to-people-with-disabilities-6f7772b2-2f33-4bd2-8ca7-dae3b2b3ef25)
  * [EPub3 with MathML](https://docs.mathjax.org/en/v2.7-latest/misc/epub.html)
* Equality Act 2010
  * Authors may need to provide additional formats to meet the needs of a specific student
  * Not all screenreaders or other assistive technology can read all accessible formats e.g. you may need to produce Word on request even if you decide not to provide this to meet the Public Sector Boddies act. 

# Formats and transforms


<!-- this will only work in large and clear print if you remove export from adjustbox, find out why -->
<div class="figure">
<iframe src="https://www.mindomo.com/mindmap/document-transforms-2d8186b662758e26ccf50ef82a3828b2?embed" width="100%" height="400px" data-external="1"></iframe>
<p class="caption">(\#fig:unnamed-chunk-1)Accessible and interactive map at https://www.mindomo.com/mindmap/document-transforms-2d8186b662758e26ccf50ef82a3828b2</p>
</div>

# Markdown

"Markdown is a text-to-HTML conversion tool for web writers. Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML (or HTML)."

John Grubber, Markdown creator
https://daringfireball.net/projects/markdown/

# RMarkdown

* Simple one page documents containing maths and/or statistics 
* RStudio provides a GUI interface
* Multiple output formats with consistent structure 
  * Accessible: HTML, Word
  * Accessible if no mathematical content: ODT, RTF
  * Inaccessible: LaTeX/PDF
  * Slides
    * Possibly accessible: PowerPoint, HTML using ioslides, reveal.js, Slidy
    * Inaccessible: LaTeX/Beamer

For further information on getting started, an example and how to test for accessibility at [RMarkdown Workshop](https://stem-enable.github.io/RMarkdownWorkshop/)
  
# Bookdown

* Designed to enable authors of **books** or longer structured documents
* Needed for:
  * Parts and appendices 
  * Finer control of figures
  * Automatic numbering and cross-referencing of figures and tables with captions 
  * Cross referencing of pieces of text
  * Equation numbering and referencing
  * Theorem and proof environments with numbering and referencing
  * Definition of custom environments
  * Citation management via Pandoc, biblatex or natbib
  * Embedding of web pages and HTML widgets
* Output to HTML book, LaTeX/PDF and EPub3 only
  * Multiple output formats but structure may be inconsistent e.g. numbering is internally consistent but may differ between formats


# ClavertonDown

* Designed to enable authors of **lecture notes** to meet the diverse needs of students by production of a consistent **set** of formats
* Needed for:
  * Bookdown features but with transformation to Word 
  * Flexible theorem-like environments akin to amsthm package in LaTeX including consistent styling, numbering and classification of type across multiple output formats
    * Numbering system of inbuilt Bookdown theorems can be changed
    * Internal references within theorem names and captions
    * Unnumbered theorem environments with original numbering
    * Shared numbering e.g. between theorem and proposition 
    * Newtheorem-type definition of theorem-like environments
    * Repeating theorem-like environments
  * Inclusion of figures in knitr engine based custom blocks, including all theorem-like, while still allowing transform to Word 
  * Supplied limited controls over visual presentation to enable a coherent set of notes with 
    * Known accessibility features
    * Clear visual markers of structure including structured colour for theorem-like environments in non-PDF formats
* Output as a mini-linked site of a set of formats which can include HTML book, HTML page, Word, EPub3, standard PDF, clear print PDF and large print PDF

# Made at Claverton Down

ClavertonDown is built by MASH, if you need something to work differently we may be able to adapt it for you. However, you should only use ClavertonDown if you cannot achieve what you need using Bookdown as going back requires you to undo all use of extra features!

* [ClavertonDown](https://bathmash.github.io/clavertondown/)
* [MASH Accessible Maths project](https://www.bath.ac.uk/projects/mathematics-accessibility/)

<!--chapter:end:index.Rmd-->

