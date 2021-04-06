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

Performance audits screenshot from Tableau version:

<img src="https://teamdocs.covid19.ca.gov/content/images/perf-tableau.png">

Vs the new version:

<img src="https://teamdocs.covid19.ca.gov/content/images/perf-v3.png">

## Screenreader support

The Tableau data visualizations aren't providing basic screenreader support:

<img src="https://teamdocs.covid19.ca.gov/content/images/screenreader-tableau.png">

This issue is solved for free in our D3 versions which use HTML for headers

<img src="https://teamdocs.covid19.ca.gov/content/images/screenreader-v3.png">

## Slow interactions

Interactions with the Tableau state dashboard are sluggish, trying to switch between statewide and county charts gives you a spinner, then displays Alameda, then shows the desired county a few seconds later. This process is so slow I can easily take a screenshot of the invalid state using my M1 mac on a fiber broadband connection.

<img src="https://teamdocs.covid19.ca.gov/content/images/tableau-wrong-county.png">

All of these issues are fixed in the V3 version.

## Octothorpes and layout weirdness

We still have a bunch of recurring weird layout problems at different screen sizes. When numbers might get clipped Tableau will replace them with a bunch of octothorpes. This often happens at very small widths. There aren't a ton of iPhone 5 users left in the wild but anybody making use of maximum screen magnification reduces their effective width to this level as well so this problem is widespread.

<img src="https://teamdocs.covid19.ca.gov/content/images/octothorpes-state-dash.png">

<img src="https://teamdocs.covid19.ca.gov/content/images/octothorpes-vaccines.png">

We often see layout problems recurring, these may be difficult to reproduce so are harder to fix. In general wrestling with responsiveness is always a hassle when deploying new Tableau charts.

<img src="https://teamdocs.covid19.ca.gov/content/images/tableau-too-wide.png">

<img src="https://teamdocs.covid19.ca.gov/content/images/tableau-overlap.png">

## Data udpates

The equity dashboard requires manual review of the scheduled data updates.

This is supervised by Dr Jason Vargo and his team from CDPH.

We create a historical record of their review by following these steps:

- The data is retrieved from snowflake on schedule and published to a staging location
- charts in our staging environment consume latest data from the staging location
- a git pull request is opened by our automatic service that notifies Dr Vargo of the new data, provides a link to the staging site to review the update using live chart code
- if the data is problematic issues are recorded in the git pull request log
- if the dats is fine approvals are recorded in the git pull request log
- The CDPH team presses merge on the pull request triggering the live data publication

<img src="https://teamdocs.covid19.ca.gov/content/images/data-updates.png">

from: <a href="https://github.com/cagov/covid-static/pull/442">equity dash pull request</a>

## More info

These shortcomings were originally detailed in <a href="https://teamdocs.covid19.ca.gov/teams/engineering/performance/">this page</a>. We shared those with Tableau, Inc. We got support from many directors working for Tableau and were able to clearly define the limitations of that tool with regards to performance and accessibility.