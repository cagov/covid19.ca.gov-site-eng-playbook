---
title: Changing text in feature card and Tracking COVID-19 in CA
date: Last Modified 
permalink: /teams/content/hero-trackerboxes.html
eleventyNavigation:
  key: Hero and trackerboxes
  parent: Homepage
  order: 236
---
The text in the homepage’s feature cardand around the Tracking COVID-19 in CA trackerboxes are maintained through the homepage labels post in WordPress.

Other text on the homepage is updated through this post, but this text rarely changes. Engineers can help you identify what rows to change if you have to update text on the homepage.

## Feature card text

The feature card text is changed in the following rows:

* varHeroTitle: The top line of text in the hero space. This is the H1 of the homepage.
* varHeroP1: The text for the arrow link in the hero space. Talk to an engineer to update the destination of this link.
* varHeroP2: The second line of text in the hero space. This is an H2.

![Hero space on the homepage](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/homepage-hero.png)

![Fields in WordPress to edit the hero space on the homepage](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/wordpress-hero.png)

## Tracking COVID-19 in CA text

The date field is automatically updated using dynamic data. This is in the varUpdateText row. We usually do not change this field.

The only field that gets modified is the line of text under the four boxes. Its default text is: _Details about this data are available in the [state dashboard](https://covid19.ca.gov/state-dashboard/)_. When there is an anomaly with the data, we add notes about it in this area. Do so by adding the desired text in front of the existing text in the _varDataDetailsHere_ row.

Always finish the content in this row with the default text. The link to the state dashboard is automatically added to the end of whatever text is in the row. 

![Tracking COVID-19 in CA boxes on the homepage](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/homepage-trackerboxes.png)

![Fields in WordPress to edit the Tracking COVID-19 in CA boxes on the homepage](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/wordpress-trackerboxes.png)
