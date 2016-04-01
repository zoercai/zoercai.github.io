---
layout: post
title: "Refactoring and Font Sizes"
date:   2015-07-07 20:03:48
categories: development
tags: typography refactoring font sizes
comments: false
published: true
---

Back from exams! So now picking up where I left off with this website. And what better way to refamiliarize myself with the structure and code of the site than to refactor? Below are notes for the site structure for my own future reference.

##There are two views:

1. **/index.html** acts as the front page of the website, and
2. **/_layouts/blog.html** displays the content in detail
 


###/index.html
uses its own stylesheet /css/styles.scss. It includes two other parts:

* /inludes/post_detail.html, which contains code for how the "Blog" section of the front page displays the latest post.
* /includes/project_slideshow.html, which contains the slideshow for the projects in the Projects section.

 

###/_layouts/blog.html
Acts as a skeleton for all blog-display-style pages, including: 

* blog post listings, project listings: which use the blog layout directly
* individual blog posts, and individual projects: which use /_layouts/post.html, which then uses the blog layout


It includes:

* Google Analytics script between <head> tags
* **/_includes/sidebar.html** which contains the sidebar content
* **/css/main.scss** which is the main Sass file and contains the variable definitions and imports all the other scss files in _sass, which are:
	* **/_sass/_base.scss:** defines the page styles
	* **/_sass/_content.scss:** defines the main content styles
	* **/_sass/_sidebar.scss:** defines the left sidebar styles
	* **/_sass/_syntax-highlighting.scss:** defines syntax highlighting

 

Turns out the code didn't need much refactoring after all. I did find several unused files which I will delete, but the rest of the code is pretty organised.

Now on to readjusting the font sizes.

The plan is to follow the idea by [CSS Tricks here](https://css-tricks.com/rems-ems/). Using px as the root font size, and rem for the individual components such as blog post containers, and finally em for the different headings and paragraphs within the containers.

I've done all the fone sizes for desktop/laptop screens today, next task: making everything responsive!