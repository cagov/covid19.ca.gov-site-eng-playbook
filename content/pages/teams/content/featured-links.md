---
title: Updating the link grid
date: Last Modified 
permalink: /teams/content/featured-links.html
eleventyNavigation:
  key: Link grid
  parent: Homepage
  order: 245
---

The link grid is located below the banner on the homepage. It is used to feature the highest-priority links on the site.

![Example of link grid on homepage](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/homepage-featured-links.jpg)

The link grid is updated through the [Homepage featured](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=10787&action=edit) WordPress post. This post uses the _fragment_ tag.

This post has more complicated markup, but editing the link text, the URL itself, or both is simple.

1. Search for the current link title to locate the featured link you want to update. The link title will have a _span class_ around it, and the corresponding _href_ will be right before the span class link title.
2. Change the text in the span class to update the link title.
3. Change the href to update the URL itself.
  a. If the link is a page on covid19.ca.gov, use the permalink slug only, followed by /.
4. Publish the post to push the changes to the site. You can use the **staging-only** tag to check the changes before publishing to the live site.

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


