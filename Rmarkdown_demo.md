R Markdown Examples
========================================================
author: Melissa Monk
date: October 2016
autosize: true

R Markdown
========================================================

In this section we're going to learn the R Markdown basics

- R Markdown renders easiest to a HTML, but we're interested
   in creating a PDF
- The assessment template is designed to only render to a PDF
- Includes flavors of R, LaTeX, and HTML
- It can be quirky at times
  * Ex. R code will still run within an HTML comment unless also commented out


How it works
========================================================

![Workflow](RMarkdownFlow.png)

When you run render, R Markdown feeds the .Rmd file to knitr, which executes all of the code chunks and creates a new markdown (.md) document which includes the code and it's output.

The markdown file generated by knitr is then processed by pandoc which is responsible for creating the finished format.

<small>Slide content from rmarkdown.rstudio.com</small>


Create an R Markdown document
========================================================
Using the generalized R markdown template, we'll walk through some examples

Do this: *File > New File > R Markdown ...*

- Give the document a title.  This is not the filename of the document and you can include spaces and punctuation.
- You will have to Save the document and assign a file name, without spaces
  * Save this in your working directory of the R project
- Accept the default Author (you can change this later)
- Change the default output to **PDF**
- Click OK


Knit, Commit, Push
========================================================
- Click on the "Knit to PDF" in the RStudio top menu.

- If all goes well, a preview version will pop-up.

- On the top right panel in RStudio, navigate to the "Git" window

- Click Commit

- Check all of the boxes of the files you want to commit.  

- Writing a commit message is required.  Once you do this, click Commit.

- You can now Push these changes to GitHub by clicking "Push"

I am only going to go through examples with PDF output, since that's what the Assessment Template uses




The YAML
========================================================
This may be the most confusing part of an R Markdown document

* The YAML is the frontmatter controlling the document and is at the very top of the file 
* The YAML starts and ends with `---`
* You cannot add comments or extraneous text to the YAML

Your YAML should look something like this:
```
yaml
---
title: "Workshop Examples"
author: "Melissa Monk"
date: "September 21, 2016"
output: pdf_document
---
```
The YAML continued
========================================================
You can change some of the YAML settings via the RStudio IDE:

Click on the "gear" in the top bar of the editor and select "Output options"

Check "Include Table of Contents"
Click "Figures" - check "Render figures with captions""
Click "Output" - check "Keep tex source..."


The YAML continued
========================================================
The YAML will now look something like this:


```
---
title: "Workshop Examples"
author: "Melissa Monk"
date: "September 21, 2016"
output: 
  pdf_document: 
    fig_caption: yes
    keep_tex: yes
    latex_engine: xelatex
    toc: yes
---
```
The YAML continued
========================================================
The YAML for the Assessment template includes additional options
Each line is described in the ReadME file
```
---
title: 'Status of Blue Rockfish (*Sebastes mystinus*) Along the U.S. Pacific Coast in x2015x'
author: ''
date: ''
output:
  pdf_document:
    fig_caption: yes
    highlight: haddock
    includes:
      before_body: Titlepage.tex
      in_header: header.tex
    keep_tex: yes
    latex_engine: xelatex
    template: Default_template_modified.tex
    number_sections: yes
    toc: yes
    toc_depth: 4
  html_document:
    toc: yes
  word_document: default
documentclass: article
fontsize: 12pt
geometry: margin=1in
csl: CJFAS.csl
bibliography: BibFile.bib
---
```



Document Sections
========================================================


Lists
========================================================


Links
========================================================


Citations
========================================================


R code chunks
========================================================


Figures
========================================================



Tables
========================================================

Referencing Tables and Figures
========================================================


Italics and Bold
========================================================



Clean up
========================================================
**Local** When you're ready to clean up, you delete the local repo any way you like. It's just a regular directory on your computer.

**GitHub** In the browser, go to your repo's landing page on GitHub. Click on "Settings".

Scroll down, click on "delete repository," and do as it asks.