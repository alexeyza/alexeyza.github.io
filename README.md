# (Obsolete) Guide for using Jekyll

## Creating a new post

A new post is simply a markdown file that looks like this:
```
---
layout: post
title:  "Welcome"
date:   2016-10-28 12:30:00
categories: [collaboration, CSCW, 'social media']
published: true
image: /assets/images/image_on_the_top_of_the_post.png
---

Content goes here
```

The post files should go into the `_posts` subfolder, and include the date of publishing as part of the filename (see example in existing files). 


## Creating a new page

Similarly to a post, a new page is simply a markdown file that looks like this:
```
---
layout: page
title: About
permalink: /about/
---

Content goes here
```

Pages should be placed in the main directory, and would be accessible at the path specified in the `permalink` above. If you want the page to be linked from the home page, you need to update the `index.html` file and a line similar to this:
```
<a href="/about/">About</a> &nbsp;&nbsp;·&nbsp;&nbsp;
```

## Running the blog locally (without deploying it)

#### Prerequisites
To run the blog locally, you must have the `Jekyll` and `Bundler` Ruby gems installed on your machine. If you don't have them, you'll need to install RVM, then install Ruby, and then using the `gem` command install `Jekyll` and `Bundler`.

#### Run Jekyll locally

All you need to do is type the following commands in terminal:
```
cd margaretstorey.github.io
bundle exec jekyll build
bundle exec jekyll serve
```

## Deploying the blog
To deploy the files to the remote and public server, just push the changes to GitHub (master branch). And wait for a few seconds until it refreshes.