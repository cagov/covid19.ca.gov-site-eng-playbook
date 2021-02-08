---
title: Code snippets
date: Last Modified 
permalink: /teams/content/code-snippets.html
eleventyNavigation:
  key: Code snippets
  parent: Editing
  order: 215
---

Below are examples of code you can use in WordPress posts. HTML can be inserted using a **Custom HTML** block. CSS classes can be added via a Block’s **Advanced** drop-down.

* Hidden question & answer
* Hidden keywords
* Action link
* Highlight box
  * Yellow alert box - DEPRECATED
* Making a header larger while preserving hierarchy
* Centering an image
* Aligning an image to the right or left of text
* Moving arrow button
* Emphasized text
* ARIA labels

## Hidden question & answer

This code creates a question & answer that will appear as a quick answer in site search, but will not appear on the page. Use sparingly, as most questions & answers would benefit users if they were seen.

```
<div style="display:none;" class="js-qa js-qa-question">Where can I find the list of essential critical infrastructure sectors?</div>

<div style="display:none;" class="js-qa js-qa-answer">Visit <a href="https://covid19.ca.gov/essential-workforce/">Essential workforce</a> to learn about what workers and sectors are included. </div>
```

## Hidden keywords

When you’d like a page or quick answer to appear in searches on a certain keyword, but you can’t seem to work that keyword into the visible text, you can add hidden keywords. The keyword below is hidden in the answer part of a quick answer.

```
<div style="display:none;" class="wp-accordion-content"><!-- curfew --></div>
```

## Action link

An action link has special styling to help it stand out. It is used for a high-priority link near the top of the page. Use only one action link per page. Using a leading icon is preferred, but optional. Always put a space after the icon.

For this action link:

![Action link](/content/images/action-link.jpg)

The code is this:

```
<a class="action-link" href="https://covid19.ca.gov/sign-up-for-county-alerts/"><span class="ca-gov-icon-warning-circle"></span><strong> Sign up for county alerts</strong></a>
```

## Highlight box

Urgent information can be highlighted at the top of a page with a highlight box. It can include a right-aligned image next to body text and an action link (button), or can stand alone without these elements.

Highlight boxes now take the place of yellow alert boxes. Use only one per page, and position at the top. Use sparingly, and get approval before publishing. Highlight boxes are an exception to page style, not a rule--there should not be one on every page.

For this highlight box with just text:

