---
title: Banner and recent updates
date: Last Modified 
permalink: /teams/content/banner.html
eleventyNavigation:
  key: Banner
  parent: Homepage
  order: 240
---

The banner and recent updates sections of the covid19.ca.gov homepage are maintained through WordPress posts.

* Banner: [new](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=1392&action=edit)
* Recent updates: [updates section homepage](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=6518&action=edit)

The recent updates section usually displays the last three banners.

## Changing the link in the banner button

The banner uses an action button link.

![Action button link in the homepage banner](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/banner-button-link-example.jpg)

Updating the link in a button requires editing in HTML view in Wordpress. This preserves the custom code that makes the link show up as a button.

1. Open the three dot menu for the link block and select **Edit as HTML**.

![Edit as HTML option in WordPress block dropdown menu](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/edit-as-html.jpg)

2. Replace the link inside the HTML chain (everything inside the quotation marks).

![Example of code to replace inside HTML view](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/button-link-html-replacement.jpg)

3. Select **Update** to send the change to production or staging as desired.
