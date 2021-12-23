---
title: Site menu
date: Last Modified 
permalink: /teams/content/menu.html
eleventyNavigation:
  key: Menu
  parent: Custom content management
  order: 233
---
The covid19.ca.gov site menu is managed through the Menu Links WordPress post. This post uses the table-data and translate tags. 

## Section names
The section names are set using the table with two columns (_section_index_ and _label_).

* The numbers in _section_index_ set the order of the sections. 1 will be the section furthest left. Additional sections are added to the right, in order.
* The content in label sets the text that shows in the menu for each section.

## Adding pages to sections
The second table with three columns (_section_index_, _label_, _slug_or_url_) is used to add links to each section.

* Links are ordered based on their order in the table. Add a row where you want the link to appear in the section drop down.
* Use the number of the section from the first table in _section_ to add a link to that section.
* Enter the text you want for the link in label.
* Add the URL for the link in _slug_ or_url_.
  * If you are adding a page on covid19.ca.gov, only enter the slug. Do not add any slashes before or after the slug.
  * If you are adding a page outside covid19.ca.gov, enter the whole URL, including _https://_ and any slashes at the end of the URL.
* **Publish** the post to push the changes to the site. You can use the _staging-only_ tag to check the menu before publishing it to the live site.
