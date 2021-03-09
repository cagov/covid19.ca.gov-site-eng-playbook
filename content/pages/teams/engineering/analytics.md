---
title: Analytics - Event Tracking
date: Last Modified 
permalink: /teams/engineering/tracking-data/index.html
eleventyNavigation:
  key: Analytics
  parent: Engineering
  order: 120
---
### Overview
There are many custom events we created to give us added context into user behavior on our site. They are all listed and defined below. These were all added at different times and the dates at which they started collecting data (or were turned off) can be deduced from Google Analytics with the date dimension. Some events are implemented globally and some are page specific, we’ll identify which are such below.  

### Event hooks conventions

If a specific query selector is needed to attach an event create a new classname with a ```js-``` prefix. Using that only for javascript event attachment makes it obvious to a developer only concerned with layout that they are affecting javascript when they are modifying HTML.

## Global event tracking

These are events that are tracked every time we spin up a new page.

### Accordion clicks

These events are attached to any of our accordion elements which can be on any page.

| Category  | Action | Label | Notes |
| ------------- | ------------- | ------------- | ------------- |
| "click"  | "accordion"  | accordion header string  | for current reporting |
| "accordion"  | "click"  | accordion header string  | for historical reporting |


### Is this page useful 

We have a widget in the footer that asks users: Is this page useful? We send events to google analytics when they click Yes or No. The comments are collected separately in a database outside of GA. The Yes/No button clicks event data is:

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "rating"  | "helpful"  | "yes" or "no"  |

### Offsite links

We record when a user clicks on a link that directs them to another url that is not on our site. e.g. https://www.cdc.gov/coronavirus/2019-ncov/vaccines/safety.html
| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "offsite"  | "url"  |

### PDF links

We record when a user clicks on a pdf link.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "pdf"  | "url"  |

### Search

We record the search terms used when searches are performed to see if we need to create more quick answer content. The "got_quick_answers" and "no_quick_answers" actions are used to show when one or more quick answers were found for the search query.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "search"  | "got_quick_answers"  | search terms  |
| "search"  | "no_quick_answers"  | search terms  |


### Surveys

We track several events related to inviting users to take surveys like the survey prompt display, clicking on the button to take the survey or dismissing the prompt.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "survey"  | "click"  | "surveyDisplay"  |
| "survey"  | "click"  | "openSurvey"  |
| "survey"  | "click"  | "dismissSurvey"  |

## Page-specific event tracking

These are events that are tied to specific pages.

### Homepage

When we redesigned and relaunched the homepage we began tracking several elements to understand what was prime real estate and what information users wanted.

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

### Safer Economy (Blueprint) page

When we launched the Safer Economy page we began tracking how users interacted with the what's open search box. If the user selected county is _(not set)_ that means they did not select a county, but are instead looking at acitivity statuses statewide. Similarly, if the user selected activity is _(not set)_ that means they are looking at all activities rather than a specific one

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "activity-status"  | <user-selected county> or (not set)  | <user-selected county> or (not set) |
