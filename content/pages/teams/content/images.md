---
title: Using images
date: Last Modified 
permalink: /teams/content/images.html
eleventyNavigation:
  key: Using images
  parent: Editing
  order: 213
---

When using images in page content, it's important to stick to certain standards to maintain a consistent look and feel sitewide. Addressed here:

* Aesthetics and style
* When to use images
* Writing captions
* Steps to adding images
* Size and resolution
* HTML for responsive images

## Aesthetics and style

For photos, design recommends full width at 5x3 aspect ratio
Illustrations/graphics should be inline or centered

## When to use images

(See content style guide for guidelines on when/why to use photos)

## Writing captions

(Text)

## Steps to adding images

* Resize and compress with Squoosh (or other tool of choice)
* Upload to Github
* Add to page in Wordpress
* Use classes in Wordpress to define desktop and mobile images

## Size and resolution concerns 

(Including accessibility through performance)

* Filesize: 
Should be as small as possible without looking like quality is being lost. Anything less than 500k is OK. 

* Image dimensions:
Desktop Width: 920px
Mobile Width: 325px

## HTML options for sharing responsive images

* using <picture /> (but needs a fallback for IE) (this format accepts multiple sizes) https://webdesign.tutsplus.com/tutorials/quick-tip-how-to-use-html5-picture-for-responsive-images--cms-21015
* Bootstrap’s .img-fluid tag reference: https://getbootstrap.com/docs/4.0/content/images/

