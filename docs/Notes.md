---
title: "RMarkdown, Bookdown or Clavertondown?"
author: 'Emma Cliffe, Skills Centre: MASH'
site: bookdown::bookdown_site
language: en
documentclass: article
classoption: a4paper
fontsize: 10pt
geometry: margin=2.5cm
output:
  clavertondown::word_clav:
    toc: true
    number_sections: true
    keep_md: true
    pandoc_args: --default-image-extension=svg
  clavertondown::epub_clav:
    toc: false
    pandoc_args: --default-image-extension=svg
  clavertondown::gitbook_clav:
    split_by: section
    keep_md: true
    config:
      download: [["Notes.html", "HTML page"], ["Notes.pdf","Standard print PDF"], ["NotesClear.pdf","Clear print PDF"], ["NotesLarge.pdf","Large print PDF"], ["Notes.docx","Accessible Word document"], ["Notes.epub","Accessible EPub book" ]]
      sharing: no
    pandoc_args: --default-image-extension=svg
  clavertondown::html_clav:
    toc: true
    pandoc_args: --default-image-extension=svg
  clavertondown::pdf_clav:
    latex_engine: pdflatex
    keep_tex: true
    fig_caption: true
    toc: true
    extra_dependencies: ["float"]
    pandoc_args: --default-image-extension=pdf
linkcolor: blue
header-includes:
  - \newcommand{\BOO}{BOO}
---

\newpage
\pagenumbering{arabic}

# An introduction {-}

* Requirements
* Formats and transforms
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

# Formats and transforms


<!-- this will only work in large and clear print if you remove export from adjustbox, find out why -->
![Figure 2.1: Accessible and interactive map at https://www.mindomo.com/mindmap/document-transforms-2d8186b662758e26ccf50ef82a3828b2](map.png){width=100%}

# RMarkdown

* Simple one page documents 
  * Accessible: HTML, Word
  * Accessible if no mathematical content: ODT, RTF
  * Inaccessible: LaTeX/PDF
* Slides
  * Possibly accessible: PowerPoint, HTML using ioslides, reveal.js, Slidy
  * Inaccessible: LaTeX/Beamer
  
# Bookdown

* Designed to enable authors of **books** or longer structured documents
* Needed for:
  * Parts and appendices 
  * Finer control of figures
  * Automatic numbering and cross-referencing of figures, tables with captions 
  * Cross referencing of pieces of text
  * Equation numbering and referencing
  * Theorem and proof environments with numbering and referencing
  * Definition of custom environments
  * Citation management via Pandoc, biblatex or natbib
  * Embedding of web pages and HTML widgets
* Output to HTML book, LaTeX/PDF and EPub3 only


# ClavertonDown

* Designed to enable authors of **lecture notes** to meet the diverse needs of students by production of a coherent **set** of formats
* Needed for:
  * Flexible theorem-like environments akin to newtheorem in LaTeX including styling, numbering and classification of type to enable structured colour
    * Numbering system of inbuilt Bookdown theorems can be changed
    * It is possible to reference other environments within theorem names
    * Unnumbered theorem environments 
    * Shared numbering e.g. between theorem and proposition 
    * Newtheorem-type definition of theorem-like environments
    * Repeating theorem-like environments
  * Inclusion of figures in WHATSIT custom blocks
  * Limited control over visual presentation to enable a coherent set of notes with 
    * Known accessibility features
    * Clear visual markers of structure
* Output as a mini-linked site of a set of formats which can include HTML book, HTML page, Word, EPub3, standard PDF, clear print PDF and large print PDF

# More information

* [ClavertonDown](https://bathmash.github.io/clavertondown/)
* [MASH Accessible Maths project](https://www.bath.ac.uk/projects/mathematics-accessibility/)

<!--chapter:end:index.Rmd-->

