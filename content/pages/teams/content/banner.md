---
title: Banner
date: Last Modified 
permalink: /teams/content/banner.html
eleventyNavigation:
  key: Banner
  parent: Homepage
  order: 240
---

The banner sections of the covid19.ca.gov homepage is maintained through a WordPress post: [new](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=1392&action=edit)

## Tags

* This post must use the fragment tag.
* It should also have the translate tag so it can be translated within a day of being updated.
* Use the _staging-only_ tag if you’d like to stage the banner first for testing.

## Changing the title and body text

1. Edit the title within WordPress as you would any text. 
  a. Make sure you do not add bold to this title. It’s an H2, so it’s already bold. Adding a bold tag will change how the font appears.
2. Edit the body text within WordPress as well.
  a. You can add a link within this body text, but it’s a best practice to keep to just one link in the banner (in the action button). 
  b. Avoid adding more than one link to the body text.


## Changing the link in the action button

The banner uses an action button link.

![Action button link in the homepage banner](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/banner-button-link-example.jpg)

Updating the link in a button requires editing in HTML view in WordPress. This preserves the custom code that makes the link show up as a button.

1. Open the three dot menu for the link block and select **Edit as HTML**.

![Edit as HTML option in WordPress block dropdown menu](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/edit-as-html.jpg)

2. Replace the link inside the HTML chain (everything inside the quotation marks).

![Example of code to replace inside HTML view](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/button-link-html-replacement.jpg)

3. Select **Update** to send the change to production or staging as desired.
