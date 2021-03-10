---
title: Data pipelines
date: Last Modified 
permalink: /teams/engineering/data-pipelines/index.html
eleventyNavigation:
  key: Data pipelines
  parent: Engineering
  order: 114
---

We run data pipelines to power data points displayed on the site homepage and dashboard pages like:

- [State dashboard](https://covid19.ca.gov/state-dashboard/)
- [Vaccines](https://covid19.ca.gov/vaccines/)
  We have docs on the data points [here](https://github.com/cagov/covid19/blob/master/src/js/vaccines/DOCS.md) 
- [Equity](https://covid19.ca.gov/equity/)

Some static data points like the numbers in boxes at the top of the homepage and state dashboard displaying cumulative numbers like case count are retrieved from Snowflake daily using our Azure functions with timer triggers like [https://github.com/cagov/Cron/tree/master/CovidStateDashboardV2](https://github.com/cagov/Cron/tree/master/CovidStateDashboardV2). These services write directly to the production branches of the covid site which triggers a new production build and deployment. These data points are trusted and so are deployed with out manual verification.

Some services are similarly automated in how they pull data but open a pull request that awaits manual merging. The tiers update does this: [https://github.com/cagov/Cron/tree/master/CovidWeeklyTierUpdate](https://github.com/cagov/Cron/tree/master/CovidWeeklyTierUpdate).

Other services power dashboards and need intensive manual review by experts before publishing. The service for the equity dashboard is one of these: [https://github.com/cagov/Cron/tree/master/CovidEquityData](https://github.com/cagov/Cron/tree/master/CovidEquityData). The Azure timer trigger runs, pulls data from snowflake, merges a PR to staging immediately and opens a PR to production which is not automatically merged. The experts are tagged on the PR so they can review the charts with latest data in staging and determine if the update should be merged or anomalies investigated. The history and discussion of their reviews along with all changes to the data are viewable in the git log.

The Snowflake SQL statements to retreive data are separated from the code which executes them and viewable here: [https://github.com/cagov/Cron/tree/master/common/SQL/CDT_COVID](https://github.com/cagov/Cron/tree/master/common/SQL/CDT_COVID)