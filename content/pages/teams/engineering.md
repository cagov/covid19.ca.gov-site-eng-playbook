---
title: Engineering
date: Last Modified 
permalink: /teams/engineering/index.html
eleventyNavigation:
  key: Engineering
  parent: Functional teams
  order: 500
---

The covid19.ca.gov site was launched in March 2020 to help the state deal with the pandemic. To balance the needs to quickly iterate on content and weather large traffic spikes the site is based on headless WordPress which triggers 11ty static site generator builds on each content change. The fully built HTML pages are deployed to static file hosts on Azure. All the code for the <a href="https://github.com/cagov/covid19">public facing site</a> and all <a href="https://github.com/cagov/Cron">services</a> which expose data sources is open source under the <a href="https://github.com/cagov">cagov</a> github account. The headless WordPress -> Static Site Generator architecture provided extra confidence in stability immediately when the site received more traffic than anticipated, moving past 100K concurrent users right after launch.

In order to ensure the pandemic response services are available to all users accessibility, performance and high quality translations are constantly prioritized. We use <a href="http://calibreapp.com/">Calibre</a> for production performance monitoring. We use both Calibre and SiteImprove for accessibility monitoring. Some advanced site features like data visualization can't yet be thoroughly audited by automated tools like this so developers still need to use screenreaders and run speed analysis checks against those features manually.

More info on user focused development is in our <a href="https://news.alpha.ca.gov/prioritizing-users-in-a-crisis-building-covid19-ca-gov/">Prioritizing users in a crisis</a> blog post. The site's high performance was featured in the <a href="https://www.youtube.com/watch?v=H89hKw06iWs&t=166s">keynote from Google's web.dev 2020</a>

Translations are provided by Avantpage's human powered translation service. We integrate with their APIs sending them the latest content directly from WordPress and receiving content in 7 languages via automated github pull requests. More info on: [translations](translations).

- Publishing pipeline
  - [11ty](eleventy/)
  - [Frontend build](frontend-build/)
  - [Content management](content-management/)

- Data sources
  - writing data into site build
  - cosmos db
  - [Public dashboards](dashboards/)
  - [Airtable](airtable/)
  - [Quick Answers](quick-answers)

- [Accessibility](accessibility/)
- [Analytics](tracking-data/)

- [Cloud infrastructure](cloud/)
- [Development code flow](devcodeflow/)
