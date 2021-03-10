---
title: Accessibility
date: Last Modified 
permalink: /teams/engineering/accessibility/index.html
eleventyNavigation:
  key: accessibility
  parent: Engineering
  order: 118
---


## Common errors

### Link text used for multiple different destinations


The same link text is used for links going to different destinations. Users might not know the difference if they are not somehow explained.


Example of this error would be two links that have the same text, such as "guidance for restaurants", however one of the links would go to web page on cdph.ca.gov website and the other one would go to a page on covid.ca.gov website.

#### How to avoid this error.

To avoid this error make sure links are distinguishable by just their link texts. For instance, if there are two links with the same text you can make first one more specific, such as "CDPH guidance for restaurants".

Another way to avoid this issue is to add some aria-label or title attribute the links. This method works if you are not authorized to alter the content. There will be no visible changes to the content; However, modifying those attributes will make those links distinguishable for the screen reader users. 

#### Check before you post
If you are an editor or a developer that are dealing with content make sure you check your page using SiteImprove accessibility checker. Publish your content to production only if it's errors free.
