---
title: Better charts
date: Last Modified 
permalink: /teams/engineering/vs-state-dash/index.html
eleventyNavigation:
  key: V3-state-dash
  parent: Engineering
  order: 105
---

<style>
#navigation {
  display: none !important;
}
#main {
  padding-left: 0 !important;
}
iframe {
  max-width: 100%;
}
.footer-nav {
  display: none !important;
}
</style>

## Performance

Time to interactive is very poor on the Tableau state dashboard, when measured using <a href="https://web.dev/measure/">https://web.dev/measure/</a> the time to interact is:

### 70 seconds

The updated D3 version of the state dashboard takes this down to:

### 4 seconds

Performance audits screenshot from Tableua version:

<img src="https://teamdocs.covid19.ca.gov/content/images/perf-tableau.png">

Vs the new version:

<img src="https://teamdocs.covid19.ca.gov/content/images/perf-v3.png">

## Screenreader support

The Tableau data visualizations aren't providing basic screenreader support:

<img src="https://teamdocs.covid19.ca.gov/content/images/screenreader-tableau.png">

This issue is solved for free in our D3 versions which use HTML for headers

<img src="https://teamdocs.covid19.ca.gov/content/images/screenreader-v3.png">

## Octothorpes

We still have a bunch of recurring weird layout problems at different screen sizes. When numbers might get clipped Tableau will replace them with a bunch of octothorpes. This often happens at very small widths. There aren't a ton of iPhone 5 users left in the wild but anybody making use of maximum screen magnification reduces their effective width to this level as well so this problem is widespread.

Performance audits screenshot from Tableua version:

<img src="https://teamdocs.covid19.ca.gov/content/images/octothorpes-state-dash.png">

<img src="https://teamdocs.covid19.ca.gov/content/images/octothorpes-vaccines.png">

## More info

These shortcomings were originally detailed in <a href="https://teamdocs.covid19.ca.gov/teams/engineering/performance/">this page</a>. We shared those with Tableau, Inc. We got support from many directors working for Tableau and were able to clearly define the limitations of that tool with regards to performance and accessibility.