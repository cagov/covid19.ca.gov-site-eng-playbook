---
title: Engineering
date: Last Modified 
permalink: /teams/engineering/index.html
eleventyNavigation:
  key: Engineering
  parent: Functional teams
  order: 500
---

The engineering team provides development support for covid19.ca.gov. 

## Open source

All of our team's code is open source. You can find everything under the <a href="https://github.com/cagov">cagov</a> github account. We have separate repositories for the <a href="https://github.com/cagov/covid19">public facing site</a> and <a href="https://github.com/cagov/Cron">services</a> that feed data to the site. We accept code changes via pull requests from partners and have had some helpful unsolicited contributions from volunteers.

## Architecture

The technical architecture is designed to: 
- cope with traffic spikes
- support frequent content updates
- prioritize fast loading on all devices
- exceed accessibility standards

In order to meet these goals we use WordPress as a headless CMS so that content editors can use a familiar, feature-rich authoring environment while giving engineers full control over code that executes in production. Content is consumed from the WordPress API on change by a serverless function that writes it directly to github and kicks off our static site generator. This builds the latest version of the full site.

More info on <a href="https://www.sanity.io/blog/headless-cms-explained">headless architecture</a>

We use web components for client-side interactivity. Using web components allow us to keep the client-side code bundle small so the site works well on low-end phones. 

We use serverless functions for data retrieval APIs. Running APIs in serverless functions lets them scale up and down to 0 by default and lets us offload all hardware and software configuration to the cloud vendor.

## Cloud hosting

The site is hosted on infrastructure managed by the California Department of Technology running on Azure/Akamai. 

## Accessibility

In order to ensure the pandemic response services are available to all users accessibility, performance and human translations are prioritized.

* We use both <a href="http://calibreapp.com/">Calibre</a> and <a href="http://siteimprove.com/">SiteImprove</a> for performance and accessibility monitoring.
* Developers also need to use screenreaders and run speed analysis checks against those features manually because automated tools don't fully cover the accessibility and performance profiling of complex features like embedded data visualizations.
 
More info on technical aspects of user focused development is in our <a href="https://news.alpha.ca.gov/prioritizing-users-in-a-crisis-building-covid19-ca-gov/">Prioritizing users in a crisis</a> blog post.

Accessibility and performance tooling is constantly evolving. Lighthouse is flexible since we can run it locally, via the command line and as an external automated service or via managed third party like Calibre we we rely on it for the first pass. 

Translations are provided by Avantpage's human-powered translation service. We integrate with their APIs sending them the latest content directly from WordPress and receiving content in 7 languages via automated github pull requests. Learn more info about [translations](translations).

## Team

The team supporting covid19.ca.gov is well versed in modern web development, creating fast-rendering websites with progressively enhanced semantic HTML, componentized javascript and CSS. We setup our own build tooling, pipeline triggers, automated testing, and API environments and specify cloud service requirements to partners.

