---
title: Quality control
date: Last Modified 
permalink: /teams/engineering/qa/index.html
eleventyNavigation:
  key: Quality control
  parent: How our team works
  order: 199
---

We attempt to ensure quality by testing on our supported browsers during development of new features, running all code changes through code review, executing automated tests as part of our continuous integration test suite, collecting and following up on production bug reports via crash catch logs and user complaints

## Supported browsers

We support the latest versions of all evergreen browsers: Chrome on desktop and mobile, Safari on desktop and mobile, Edge on desktop, Firefox on desktop.

We also still test on IE11

## Progressive enhancement

Using progressive enhancement patterns to make sure that features can fail gracefully is helpful when there are bugs or we want to utilize features not supported by older browsers.

Our accordions are an example. These require javascript, we code them in ES6 and transpile to ES5 for IE11 but if for some reason the javascript does not execute the accordions default state is expanded so a client side code malfunction will not prevent users from accessing the content.

## Code reviews

Any code change will be made as a pull request, all engineers on the team are invited to review the update so we can keep up to date with the codebase, spot bugs and learn from each other.

## CI

We have automated end to end tests that run on every pull request. These interact with the site using a headless browser engine so they can check that pages have rendered completely and that client side code like google analytics events triggered on user clicks are firign.

## Crash logs

We follow the error tracking method specified by <a href="https://philipwalton.com/articles/the-google-analytics-setup-i-use-on-every-site-i-build/#error-tracking">philip walton</a> which sends error reports to google analytics. This helps by collecting error reports in an existing location and prevents us from having to install and deliver a separate error tracking library.

## User feedback

Per page user feedback is available at the bottom of every page. We have live views of this available for review by the editorial content team and filter the reports by page assignment. We receive quite a bit of user feedback on every url every day, user pain points are identified and addressed.