---
title: Post with Autonumbering and TOC On
description: Example of post with autonumbering sections and subsections of article with autonumbering true frontmatter 
date: 2020-06-25
author: authorA
categories:
  - "Category2"
autonumbering: true
---

This article is to demonstrate the use of `autonumbering` flag in frontmatter to make your sections and subsections autonumbered by CSS
<!--more-->

## Section 1
This is the first section of your article. Just see the numbering `1.` auto applied to this section.

If your `toc` flag is on in frontmatter then `autonumbering` flag also autonumbered sections and subsections title in table of content (page content).

Also note that we generally start our sections with `<h2>` HTML elements since `<h1>` is reserved for post title.

### Subsection 1
This is first sub section of first section of your article. Just see the autonumbering `1.1` auto applied to this sub section.

#### SubSubSection 1
This is first subsub section of first sub section of your article. Just see the autonumbering `1.1.1` auto applied.

##### 5th Level
We have enabled autonumbering to first three levels. Autonumbering will not be applied to this nested section. If you wish you apply autonumbering to this section and subsequent level sections and tweak the `/css/style.css`

##### 6th Level
Autonumbering is not applied here as well.

### Subsection 2
This is second sub section of first section of your article. Just see the autonumbering `1.2` auto applied to this sub section.

## Section 2

### Subsection 1

### Subsection 2


## Section 3

### Subsection 1

### Subsection 2