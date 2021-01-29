---
title: Analytics
date: Last Modified 
permalink: /analytics/index.html
eleventyNavigation:
  key: Analytics
  order: 0
  title: Analytics implementation
---

## Event hooks conventions

If a specific query selector is needed to attach an event create a new classname with a ```js-``` prefix. Using that only for javascript event attachment makes it obvious to a developer only concerned with layout that they are affecting javascript when they are modifying HTML.

## Accordion clicks

These events are attached to any of our accordion elements which can be on any page

| Category  | Action | Label | Notes |
| ------------- | ------------- | ------------- | ------------- |
| "click"  | "accordion"  | accordion header string  | for current reporting |
| "accordion"  | "click"  | accordion header string  | for historical reporting |


## Is this page useful

We have a widget in the footer that asks users: Is this page useful? We send events to google analytics when they click Yes or No. The comments are collected separately in a database outside of GA. The Yes/No button clicks event data is:

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "rating"  | "helpful"  | "yes" or "no"  |

## Offsite links

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "offsite"  | url  |

## pdf links

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "click"  | "pdf"  | url  |

## Search

We record the search terms used when searches are performed to see if we need to create more quick answer content. The "got_quick_answers" and "no_quick_answers" actions are used to show when one or more quick answers were found for the search query

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "search"  | "got_quick_answers"  | search terms  |
| "search"  | "no_quick_answers"  | search terms  |


## Surveys

We track several events related to inviting users to take surveys like the survey prompt display, clicking on the button to take the survey or dismissing the prompt.

| Category  | Action | Label |
| ------------- | ------------- | ------------- |
| "survey"  | "click"  | "surveyDisplay"  |
| "survey"  | "click"  | "openSurvey"  |
| "survey"  | "click"  | "dismissSurvey"  |
