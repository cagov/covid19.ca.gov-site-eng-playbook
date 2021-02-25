---
title: WIP - What's open search data
date: Last Modified 
permalink: /teams/content/whats-open.html
eleventyNavigation:
  key: What's open
  parent: Blueprint
  order: 252
---

Almost everything related to the what's open search is managed through WordPress posts that are labeled as _fragments_. The exception are the county tiers themselves, which are updated by the development team.

## Update schools tier

1. Schools data lives separately from what’s open data.
  a. This in the **Schools may reopen in these counties** WordPress file.
  b. The list is updated based on the county tier Excel spreadsheet, specifically column H which will indicate _May Reopen_ if allowed to be open.
2. Check all _May Reopen_ counties against the list in WordPress.
3. If a county has been added, use the **Edit table** button to add a new row.
  a. Add counties in alphabetical order to make the table easy to maintain.
4. If a county has been removed, use the **Edit table** button to delete its row.
5. Stage the update by adding the _staging-only_ tag to the _Document_ panel on the right and selecting **Update**.
6. Check the staged version to ensure that the appropriate counties are showing the right status.
7. Publish the update by removing the _staging-only_ tag and pressing **Update**.
8. This work has a lag time to publication and usually requires a purge by a developer to ensure that multiple updates publish when expected.

## Update what’s open data

Content lives in two places: the _Data for What's Open Search_ Google Sheet (where we track in progress changes) and WordPress file titled _What’s open data_ (what shows up on the Blueprint page).

The Google Sheet's **Data for What’s Open...** tab is where the current data lives.

* The _Category_ is usually the Industry Guidance accordion for that activity.
* The link in the Industry guidance column is used in WordPress.
  * Consult with the Industry guidance content captain for what guidance to link with what activity.
  * Guidance links are anchor links to the specific accordions on our Industry guidance webpage. See [Industry guidance: Anchor links](https://docs.google.com/document/d/1HQIg2FNAxGnjGs9jPFCrFXs1XvN17d_ojHrnfZvvLus/edit) for a complete list.
* Column H are notes that only the content team uses. Update these as we see fit.
* Rows in lime color denote what’s about to change or a change that is holding for final approval from the Governor’s office.
* Rows in gray indicate that the activity’s approval was reversed or not approved. We keep it there for reference or in case that changes.
* If the only change to an activity is the PDF being updated, there’s no update needed to what’s open data.
* The Governor’s office usually does not provide statuses or details in a uniform way. It is up to the content team to provide uniformity while still being accurate.
* Ignore the schools row in the Google Sheet.
* While conversations are in progress, edit the Google Sheet instead of the WordPress file as this is easier.

The WordPress **What’s open data file** is where we make changes that are reflected on the live site.

* Use the **Edit table** button to add a row if a new activity is being added.
* Columns go worst tier to best tier, left to right. (Note that the columns are numbered incorrectly, but do not change that.)
* There are two columns to the right that are obscured (one can partially be seen and one cannot).
  * If tabbing over in the table to the far right columns does not work, use the scroll bar at the bottom of the table in WordPress.
* Column 5 is where the industry guidance link goes.
  * You cannot copy and paste into this column. There is custom formatting that needs to be present.

To add or edit column 5 data:

1. Select the triple dot icon in the header menu (to the right of the gear icon) and select **Code editor**. This will show the raw HTML of the page.
2. Moving to Code editor will always take you to the top of the page. To find the content you want to edit, use your browser’s **Search** or **Find in this page** function (usually in the **Edit** menu).
3. The link to edit is always the last td and /td set before /tr.
4. Copy the code for another industry guidance link and modify that.
  a. Do not use an ampersand in any descriptions of the guidance (like Amusement parks and theme parks).
  b. Copy and paste that into the new td /td section.
    i. Make sure you do not accidentally put an extra set of td and /td in when you copy and paste.
  d. Return to the **Visual editor** through the three dot button. If the code is acceptable, the cell will be white. If it is not, the cell will be gray.
5. Confirm all industry guidance links with the industry guidance content captain.
6. Publication of what’s open data usually takes some time. A noon deadline for publication requires publishing by 11:30 am Pacific.
  a. It's usually not possible to stage the changes as it takes 20 minutes for the changes to reach the staging server.
  b. Changes can come in as late as 11:15 am Pacific.
  c. What’s open data takes longer to publish than the Industry guidance page, so publish what’s open data before Industry guidance to try to time them to update at the same time.
7. Begin working on the WordPress file no later than 11:00 am Pacific as it takes time to get the data in due to the size of the file.

## Regional Stay Home Order tiers

The Regional Stay Home Order triggered when a region fell below 15% ICU beds available. This resulted in counties being put into a new status outside of the regular Blueprint tiers. The Regional Stay Home Order is no longer in effect, but the process for moving a region under the Order in the what's open search is as follows:

To update the activities allowed in all counties in that region, go to the [RSHO post](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=7402&action=edit) in WordPress and add the region name. You need the exact region name, which can be found by searching on one of the affected counties in the what’s open search and checking its tile.

![Example of county with region](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/region-example.jpg)

* Once the region is added to this post and published, the what’s open search will return RSHO activity data for the counties in that region.
