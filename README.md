# hugo-theme-highway
Highway is a theme for [Hugo](https://gohugo.io/), a static site generator.

## Overview
* Highway theme use [Hugo Mainroad Theme](https://themes.gohugo.io/mainroad/) as a base and add many features.
* Highway theme is an initiative taken while building a website [CodingNConcept](https://codingnconcepts.com/) with all the features available in the theme.

## Features
1. [Client Side Search Engine](https://codingnconcepts.com/hugo/client-side-search-engine-hugo/)
2. [Multiple Author Support for Blog Website](https://codingnconcepts.com/hugo/multiple-authors-hugo/)
3. [Authonumbering of Headings and subheadings in Blog Posts](https://codingnconcepts.com/hugo/auto-number-headings-hugo/)
4. [Nested Menu for Website Navigation](https://codingnconcepts.com/hugo/nested-menu-hugo/)
5. [Social Share Icons for Blog Posts](https://codingnconcepts.com/hugo/social-icons-hugo/)
6. [Google Analytics](https://codingnconcepts.com/hugo/custom-google-analytics-hugo/)
7. [RSS Feed](https://codingnconcepts.com/hugo/custom-rss-feed-hugo/)
8. [sitemap.xml for SEO](https://codingnconcepts.com/hugo/sitemap-hugo/)
9. [JSON+LD for SEO](https://codingnconcepts.com/hugo/structure-data-json-ld-hugo/)
10. [Useful ShortCodes](https://codingnconcepts.com/hugo/custom-shortcode-hugo/)

## Run Example Site

Clone the hugo-theme-highway github repo and run the example site with following commands:-
```
git clone https://github.com/ashishlahoti/hugo-theme-highway.git
cd hugo-theme-highway
hugo server --source exampleSite --themesDir ../..
```

## Create Hugo Website with Highway Theme
### Step 1: Install Git and Hugo
If you are using MacOS, then you can install [Homebrew](https://brew.sh/) package manager and run following commands from terminal:-
1. To install Git, run  `brew install git`
2. To install Hugo, run `brew install hugo`

If you are using Windows or Other Operation System, then you can install them with these links:-
1. [Git](https://git-scm.com/downloads)
2. [Hugo](https://gohugo.io/getting-started/installing) 

### Step 2. Create a New Site
```
hugo new site quickstart
```
The above will create a new Hugo site in a folder named `quickstart`.

### Step 3: Add Highway Theme
First, download the theme from GitHub and add it to your site’s `themes` directory:

```
cd quickstart
git init
git submodule add https://github.com/ashishlahoti/hugo-theme-highway.git themes/highway
```

Note for non-git users:

* If you do not have git installed, you can download the archive of the latest version of this theme from: https://github.com/ashishlahoti/hugo-theme-highway/archive/master.zip
* Extract that .zip file to get a “hugo-theme-highway-master” directory.
* Rename that directory to "highway", and move it into the “themes/” directory.

Then, add the theme to the site configuration:

```
echo theme = \"highway\" >> config.toml
```

>Note: If you do not want to use Highway theme then See [themes.gohugo.io](https://themes.gohugo.io/) for a list of themes to consider. Steps to use any other theme would be same.

### Step 4: Add Some Content 
You can manually create content files (for example as `content/<CATEGORY>/<FILE>.<FORMAT>`) and provide metadata in them, however you can use the `new` command to do a few things for you (like add title and date):

```
hugo new posts/my-first-post.md
```

Edit the newly created content file if you want, it will start with something like this:

```
---
title: "My First Post"
date: 2019-03-26T08:47:11+01:00
draft: true
---
```

Drafts do not get deployed; once you finish a post, update the header of the post to say `draft: false`.

### Step 5: Start the Hugo server 
Now, start the Hugo server with drafts enabled:
```
hugo server -D
```
Navigate to your new site at http://localhost:1313

### Step 6: Build Static Site
Now time to generate static website from Hugo pages. Just run:
```
hugo -D
```
Output will be in `./public/` directory by default (`-d/--destination` flag to change it, or set publishdir in the config file).


## Host Hugo Website on Github 
You will find it interesting that you can host one website per Github account for FREE!

Follow these simple [steps](https://pages.github.com/) to host your website.

Other Useful links for Github:-

https://docs.github.com/en/github/managing-files-in-a-repository/adding-a-file-to-a-repository


