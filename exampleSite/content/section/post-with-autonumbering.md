---
title: Post with Auto Numbering
date: 2020-06-29
author: authorA
categories:
  - "Category2"
# Theme-Defined params
comments: false # Enable Disqus comments for specific page
authorbox: true # Enable authorbox for specific page
toc: true # Enable Table of Contents for specific page
mathjax: false # Enable MathJax for specific page
socialshare: false # Enable social share links after post for specific page
autonumbering: true # Enable Autonumbering of sections and subsections for specific page
thumbnail: "/img/favicon.ico" # Thumbnail to be displayed with Post Title
---

This article demonstrates, how to enable `autonumbering` in your blog post to make post's sections and subsections auto-numbered by CSS
<!--more-->

## Autonumbering
By default, autonumbering is disabled for the post. You can enable autonumbering by adding `autonumbering: true` in the front-matter.

Just see the numbering `1.` auto applied to this section.

Also note that we generally start our sections with `<h2>` HTML elements since `<h1>` is reserved for post title.

### Autonumbering with TOC
If you have enabled TOC (Table of Content, or Page Content) in your post by adding `toc: true` in the front-matter. Then autonumbering will be applied to TOC as well.

Just see the numbering `1.1` auto applied to this sub-section.

### Autonumbering levels
Autonumbering is applied for `<h2>`, `<h3>` and `<h4>` headings only. If you wish to apply autonumbering to `<h5>` and `<h6>` headings then update the following CSS in `/themes/highway/assets/style.css`

```css
/* Auto Numbering */
body {counter-reset: h2}
h2 {counter-reset: h3}
h3 {counter-reset: h4}
h4 {counter-reset: h5}
h5 {counter-reset: h6}

article[autonumbering] h2:before {counter-increment: h2; content: counter(h2) ". "}
article[autonumbering] h3:before {counter-increment: h3; content: counter(h2) "." counter(h3) ". "}
article[autonumbering] h4:before {counter-increment: h4; content: counter(h2) "." counter(h3) "." counter(h4) ". "}
article[autonumbering] h5:before {counter-increment: h5; content: counter(h2) "." counter(h3) "." counter(h4) ". " counter(h5) ". "}
article[autonumbering] h5:before {counter-increment: h6; content: counter(h2) "." counter(h3) "." counter(h4) ". " counter(h5) ". " counter(h6) ". "}


article[autonumbering] .toc__menu ul { counter-reset: item }
article[autonumbering] .toc__menu li a:before { content: counters(item, ".") ". "; counter-increment: item }
```

## `<h2>` heading auto numbering

Auto-numbering `2.` is applied to `<h2>` heading

### `<h3>` heading auto numbering

Auto-numbering `2.1` is applied to `<h3>` heading

#### `<h4>` heading auto numbering

Auto-numbering `2.1.1` is applied to `<h4>` heading

##### `<h5>` heading no numbering
Auto-numbering is not applied to `<h5>` heading

##### `<h6>` heading no numbering
Auto-numbering is not applied to `<h6>` heading

### Another `<h3>` heading

Auto-numbering `2.2` is applied to `<h3>` heading


## Section 3

### Subsection 1

### Subsection 2