Assessment Template
========================================================
author: Melissa Monk
date: October 2016
autosize: true

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

Slide With Code
========================================================


```r
summary(cars)
```

```
     speed           dist       
 Min.   : 4.0   Min.   :  2.00  
 1st Qu.:12.0   1st Qu.: 26.00  
 Median :15.0   Median : 36.00  
 Mean   :15.4   Mean   : 42.98  
 3rd Qu.:19.0   3rd Qu.: 56.00  
 Max.   :25.0   Max.   :120.00  
```

Slide With Plot
========================================================

![plot of chunk unnamed-chunk-2](Assessment_template_demo-figure/unnamed-chunk-2-1.png)
