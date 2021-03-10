---
title: Engineering
date: Last Modified 
permalink: /teams/engineering/index.html
eleventyNavigation:
  key: Engineering
  parent: Functional teams
  order: 500
---
<!--

Before you get into the bullet list like publishing pipeline, data sources, etc…. Add in intro to that laundry list (as its different from your left nav). Is this quick links to get to sections they’re looking for? Or its supposed to be the nav (and then if that’s the case, update the left page nav to show this pls!)
Do you want to add an about the team somewhere? - like what skills/experience (short paragraph) the team comprises of / what is necessary to run this site?

-->

The covid19.ca.gov site was launched in March 2020 to help the State of California deal with the pandemic. 

## Open source

All of our team's code is open source. You can find everything under the <a href="https://github.com/cagov">cagov</a> github account. We have separate repositories for the <a href="https://github.com/cagov/covid19">public facing site</a> and <a href="https://github.com/cagov/Cron">services</a> which feed data to the site. We accept code changes via pull requests from partners and have had some helpful unsolicited contributions from volunteers.

## Architecture

The technical architecture is designed to cope with traffic spikes, frequent content updates, to prioritize fast loading on all devices and to exceed accessibility standards. In order to meet these goals we use WordPress as a headless CMS so that content editors can use a familiar, feature rich authoring environment but we can have full control over code that executes in production. Content is consumed from the WordPress API on change by a serverless function which writes it directly to github and kicks off our static site generator. This builds the latest version of the full site we can host on the cheapest, easiest to secure and manage, and most easily scalable cloud service. The headless WordPress -> Static Site Generator architecture provided extra confidence in stability immediately when the site received more traffic than anticipated, moving past 100K concurrent users right after launch.

We use web components for client side interactivity and serverless functions for data retrieval APIs. Writing our own web components and using other low dependency web components allow us to keep the client side code bundle small so the site works well on low end phones. Running APIs in serverless functions lets them scale up and down by default and let us offload all hardware and software configuration to the cloud vendor.

## Cloud hosting

The site is hosted on infrastructure managed by the California Department of Technology running on Azure/Akamai. 

## Accessibility

In order to ensure the pandemic response services are available to all users accessibility, performance and human translations are prioritized. We use <a href="http://calibreapp.com/">Calibre</a> for production performance monitoring. We use both Calibre and SiteImprove for accessibility monitoring. Developers also need to use screenreaders and run speed analysis checks against those features manually because automated tools don't fully cover the accessibility and performance profiling of complex features like embedded data visualizations. More info on technical aspects of user focused development is in our <a href="https://news.alpha.ca.gov/prioritizing-users-in-a-crisis-building-covid19-ca-gov/">Prioritizing users in a crisis</a> blog post. Accessibility and performance tooling is constantly evolving. Lighthouse is flexible since we can run it locally, via the command line and as an external automated service or via managed 3rd party like Calibre we we rely on it for the first pass. 

Translations are provided by Avantpage's human powered translation service. We integrate with their APIs sending them the latest content directly from WordPress and receiving content in 7 languages via automated github pull requests. More info on: [translations](translations).


## Team

The team supporting the covid19.ca.gov site is well versed in modern web development, creating fast rendering websites with progressively enhanced semantic HTML, componentized javascript and CSS. We setup our own build tooling, pipeline triggers, automated testing and API environments and specify cloud service requirements to partners.

## Content

- [11ty](eleventy/)
- [Frontend build](frontend-build/)
- [Content management](content-management/)

## Data

- [Data pipelines](data-pipelines/)
- [Surveys and feedback](surveys)
- [Public dashboards](dashboards/)
- [Airtable](airtable/)
- [Quick Answers](quick-answers)

## Development

- [Accessibility](accessibility/)
- [Analytics](tracking-data/)
- [Cloud infrastructure](cloud/)
- [Development code flow](devcodeflow/)
