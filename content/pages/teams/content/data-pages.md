---
title: Data pages
date: Last Modified 
permalink: /teams/content/autoformat.html
eleventyNavigation:
  key: Data pages
  parent: Editing
  order: 218
---
Covid19.ca.gov has three data pages:

* [State dashboard (Tracking COVID-19 in California)](https://covid19.ca.gov/state-dashboard/)
* [Health equity (California’s commitment to health equity)](https://covid19.ca.gov/equity/)
* [Vaccination data](https://covid19.ca.gov/vaccination-progress-data/)

The paragraph text on these pages is maintained like a regular page.

If you need to change the text inside of a data chart, you may need to work with an engineer. The exception is if the chart uses D3, which you may be able to edit text in WordPress. When in doubt, ask an engineer for help. They’ll show you what you can and cannot change.

If the chart uses Tableau, it will have a bar at the bottom of the chart with the word Tableau on the left. These are maintained by the Snowflake team, which works with the California Department of Public Health. Talk to them about making changes to the chart text.

## Source data

Every chart gets a link to the source data on the Open Data Portal. Use this code to create the link, modifying as appropriate.

```
<p class="small-text mt-2"><a href="https://data.chhs.ca.gov/dataset/covid-19-time-series-metrics-by-county-and-state">Confirmed cases and deaths source data</a></p>
```

## Chart information accordion

Use a chart information accordion if you need to provide details about the chart. This hides them from the view of most visitors (who likely are not interested), but makes them available close to the chart for people who are.

The chart information accordion is available as a preformatted block. It’s called **chart-drawer-covid19.ca.gov** block. All you need to add is the text in the body of the accordion. You can use paragraph and list formatting inside the accordion.
