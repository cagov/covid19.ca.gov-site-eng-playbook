---
title: Updating featured links
date: Last Modified 
permalink: /teams/content/featured.html
eleventyNavigation:
  key: Featured
  parent: Homepage
  order: 250
---

The featured links are located below the banner on the homepage:

![Example of featured links location on homepage](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/homepage-featured-links.jpg)

The featured links are updated through the [Homepage featured](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=10787&action=edit) WordPress post.

This post has more complicated markup, but editing the link text, the URL itself, or both is simple.

1. Search for the current link title to locate the featured link you want to update. The link title will have a _span class_ around it, and the corresponding _href_ will be right before the span class link title.
2. Change the text in the span class to update the link title.
3. Change the href to update the URL itself.

**Example of changing a featured link title and updating an internal URL**

Before: 

![Example of updating featured link title and internal URL before](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/example-updating-featured-link-before.jpg)

After: 

![Example of updating featured link title and internal URL after](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/example-updating-featured-link-after.jpg)

**Example of updating an internal URL to an external URL**

Before:

![Example of updating featured link internal URL to external URL before](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/example-changing-to-external-link-before.jpg)

After:

![Example of updating featured link internal URL to external URL after](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/example-changing-to-external-link-after.jpg)


