---
title: Surveys
date: Last Modified 
permalink: /teams/engineering/surveys/index.html
eleventyNavigation:
  key: Surveys
  parent: Engineering
  order: 115
---

We collect user feedback in a few different ways.

## Top of page surveys

These are displayed at the top of the site and lead to SurveyMonkey forms. We have different surveys running at different times and frequencies. Sometimes there are translated versions presented on translated versions of pages. The translated survey URLs may be controlled via the [common page labels](https://github.com/cagov/covid19/blob/master/pages/wordpress-posts/common-page-labels.json) file controlled from WordPress data tables.

## Per page feedback

This is integrated into the bottom of every page. It collects:

  * A yes/no response to _Did you find what you were looking for?_ data point that is transmitted to Google Analytics as an event with the action _feedback_
  * The yes/no response and any text field explanation which is sent to Azure CosmosDB and viewable in our [feedback review site](https://github.com/cagov/comment-reports)

## Ethnio intercepts

We can run ethnio-powered surveys in pages. These integrations are performed by adding the ethnio tag to the WordPress post we want ethnio to appear on. These survey runs have been temporary so we remove the ethnio tag when the run on that page is complete.
