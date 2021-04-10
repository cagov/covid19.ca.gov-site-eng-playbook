---
title: Accessibility
date: Last Modified 
permalink: /teams/engineering/accessibility/index.html
eleventyNavigation:
  key: Accessibility
  parent: How our team works
  order: 120
---

Here are some common accessibility errors.

## Link text used for multiple different destinations

The same link text is used for links going to different destinations. Users might not know the difference between the links. An example of this error would be two links that have the same text, such as _guidance for restaurants_, but one of them goes to a web page on cdph.ca.gov and the other goes to a PDF hosted on covid.ca.gov.

### How to fix

Make sure links are distinguishable by just their link text. To fix the example above, make the first link _CDPH guidance for restaurants_.

Another way to avoid this issue is to add an aria-label or title attribute the links. This method works if you are not authorized to change the content. There will be no visible changes to the content, but modifying those attributes will make those links distinguishable for the screenreader users. 

## Check before you post

Check your page using [SiteImprove](https://my2.siteimprove.com/Dashboard/5765905975/20288807517/Dashboard/Index). Publish your content to production only if it's error-free.
