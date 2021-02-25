---
title: County map dates
date: Last Modified 
permalink: /teams/content/map-dates.html
eleventyNavigation:
  key: Map dates
  parent: Blueprint
  order: 253
---

The county map on [Blueprint for a Safer Economy](https://covid19.ca.gov/safer-economy/) and the [state dashboard](https://covid19.ca.gov/state-dashboard/) has two dates that must be updated whenever new tier assignments are released. These updates are made in a WordPress post that updates both locations at once.

![The county map with the date fields](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/county-map-dates.jpg)

To find out what dates to use, get the Excel file that is emailed for the day’s tier assignment. (If you’re not on this thread, ask the product lead.) Locate these two dates:

![Excel Sheet showing where to find each needed date](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/tier-spreadsheet-dates.jpg)

To change these dates:

1. Open WordPress and select the post titled [Schools may reopen in these counties](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=6422&action=edit).
2. Scroll to the bottom of the post and find the table labeled Update these dates as tier data changes.
3. The _TIER_DATE_ column is used to update the date in the header (_Current tier assignments as of [TIER_DATE]_). The _TIER_ENDDATE_ column is used to update the date in the footer (_All data and tier assignments are based on results from week ending [TIER_ENDDATE]_.)
  a. Replace the existing dates with the new dates. Use this format: _YYYY-MM-DD_.
4. Select **Update** pushes these changes to production without needing to republish Blueprint or the state dashboard. To stage these changes, add the **staging-only** tag to the post.
