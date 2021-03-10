---
title: Surveys
date: Last Modified 
permalink: /teams/engineering/surveys/index.html
eleventyNavigation:
  key: Surveys
  parent: Engineering
  order: 115
---

We collect user feedback from:
- surveys displayed at the top of the site that lead to surveymonkey forms
  We have different surveys running at different times and displayed at different frequencies, sometimes there are translated versions of these presented on translated versions of pages. The translated survey urls may be controlled via the <a href="https://github.com/cagov/covid19/blob/master/pages/wordpress-posts/common-page-labels.json">common page labels</a> file controlled from WordPress data tables.

- The feedback form integrated into the bottom of every page.
  This form collects:
    - A Yes/No response to "Did you find what you were lookinf for?" data point that is transmitted to GA as an event with the action: feedback
    - The Yes/No response and a text field explanation which is sent to Azure CosmosDB and viewable in our <a href="https://github.com/cagov/comment-reports">feedback review site</a>

- We run ethnio powered surveys in pages as well. These integrations are performed by adding the ethnio tag to the WordPress post content of the page we want ethnio to appear on. These survey runs have been temporary so we remove the ethnio tag when the survey run on that page is complete.