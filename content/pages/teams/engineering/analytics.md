---
title: Event tracking analytics
date: Last Modified 
permalink: /teams/engineering/tracking-data/index.html
eleventyNavigation:
  key: Event tracking analytics
  parent: User Interaction Information
  order: 121
---

There are many custom events we created to give us added insight into user behavior. They are listed and defined below. These were added at different times and the dates at which they started collecting data (or were turned off) can be deduced from Google Analytics with the date dimension. Some events are implemented globally and some are implemented at a page-level, we’ll identify which are such below.  

## Event hooks conventions

If a specific query selector is needed to attach an event create a new classname with a **js-** prefix. Using that only for javascript event attachment makes it obvious to a developer only concerned with layout that they are affecting javascript when they are modifying HTML.

## Accordion clicks - global

These events are attached to any of our accordion elements, which can be on any page.

| Category  | Action | Label | Notes |
| ------------- | ------------- | ------------- | ------------- |
| "click"  | "accordion"  | accordion header string  | for current reporting |
| "accordion"  | "click"  | accordion header string  | for historical reporting |

## Is this page useful - global

We have a widget in the footer that asks users _Is this page useful?_ We send events to Google Analytics when they click _Yes_ or _No_. The comments are collected separately in a database outside of Google Analytics. The _Yes/No_ button clicks event data is:

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "rating"  | "helpful"  | "yes" or "no"  |

## Offsite links - global

We record when a user clicks on a link that send them to a URL that's not on our site (for example, https://www.cdc.gov/coronavirus/2019-ncov/vaccines/safety.html).

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "offsite"  | "url"  |

## PDF links - global

We record when a user clicks on a PDF link.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "pdf"  | "url"  |

## Search - global

We record the search terms people use to see if we need to create more quick answer content. The _got_quick_answers_ and _no_quick_answers_ actions are used to show when a search query finds one or more quick answers.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "search"  | "got_quick_answers"  | search terms  |
| "search"  | "no_quick_answers"  | search terms  |

## Surveys - global

We track several events related to inviting users to take surveys like the survey prompt display, selecting on the button to take the survey, or dismissing the prompt.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "survey"  | "click"  | "surveyDisplay"  |
| "survey"  | "click"  | "openSurvey"  |
| "survey"  | "click"  | "dismissSurvey"  |

## Home - page-level

When we redesigned and relaunched the [homepage](https://covid19.ca.gov/) we began tracking several elements to understand what was prime real estate and what information users wanted.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "homepage-tracking covid"  | "url"  |
| "click"  | "homepage-hero text"  | "url"  |
| "click"  | "homepage-alerts section"  | "url"  |
| "click"  | "homepage-want to know"  | "url"  |
| "click"  | "homepage-footer"  | "url"  |
| "click"  | "homepage-menu"  | "url"  |
| "click"  | "homepage-video"  | "url"  |
| "click"  | "homepage-latest news"  | "url or 'view more'"  |
| "scroll"  | "scroll-25" | "scroll-25-homepage" |
| "scroll"  | "scroll-50" | "scroll-50-homepage" |
| "scroll"  | "scroll-75" | "scroll-75-homepage" |
| "scroll"  | "scroll-90" | "scroll-90-homepage" |

## Safer Economy (Blueprint) - page-level

When we launched the [Blueprint for a Safer Economy page](https://covid19.ca.gov/safer-economy/) we wanted to track how users interacted with the what's open search box. If the user selected county is _(not set)_ that means they did not select a county and are looking at acitivity statuses statewide. Similarly, if the user-selected activity is _(not set)_ that means they are looking at all activities rather than a specific one.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "activity-status"  | "{user-selected-county}" or "(not set)"  | "{user-selected-activity}" or "(not set)" |

## Equity - page-level

When we launched the [equity page](https://covid19.ca.gov/equity/) we wanted to track how users interacted with the page and chart data.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "activity-status"  | "county-select" | "{user-selected-county}" |
| "click"  | "tab-select" | "chart-name" |
| "scroll"  | "scroll-25" | "scroll-25-equity" |
| "scroll"  | "scroll-50" | "scroll-50-equity" |
| "scroll"  | "scroll-75" | "scroll-75-equity" |
| "scroll"  | "scroll-90" | "scroll-90-equity" |
| "scroll"  | "chart-in-view" | "chart-name" |


## CTA

We are tracking some call to action links with custom events. There is javascript tracking code that will look for the cta data attribute and apply a click listener that fires a custom event so you can instrument links as follows:

Example:
```
<a href="https://myturn.ca.gov/" class="link-arrow-blue text-center" data-tracking-action="cta" data-tracking-label="$15 million">
  <div class="link-arrow-label">GET VAXED TO WIN</div>
  <cagov-arrow></cagov-arrow>
</a>
```

The important parts are:

- data-tracking-action="cta" 

This should be the same on every link. The string cta needs to be used for the javascript event assignment to find the link. This will fire a custom event on click with an action value of cta and a category value of click.

- data-tracking-label="$15 million"

This value should be set to the string you want to show up in google analytics as the event label value. 