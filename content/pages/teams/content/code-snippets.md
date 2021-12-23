---
title: HTML code samples
date: Last Modified 
permalink: /teams/content/code-snippets.html
eleventyNavigation:
  key: HTML code samples
  parent: Editing
  order: 215
---

Below are examples of code you can use in WordPress posts. HTML can be inserted using a **Custom HTML** block. [CSS classes](https://teamdocs.covid19.ca.gov/teams/content/classes.html) can be added via a Block’s **Advanced** drop-down when they apply to a whole block, or inserted into an HTML tag when they do not. If you're looking for something that is not listed here, check the [components](https://teamdocs.covid19.ca.gov/components/) section of this site.

* [Hidden question & answer](#hidden-question-and-answer)
* Hidden keywords

## Hidden question and answer

You can create a question & answer that appears as a quick answer in site search, but does not appear on the page. Use this sparingly, as most questions & answers would benefit people if they are seen on pages.

```
<div style="display:none;" class="js-qa js-qa-question">Where can I find the list of essential critical infrastructure sectors?</div>

<div style="display:none;" class="js-qa js-qa-answer">Visit <a href="https://covid19.ca.gov/essential-workforce/">Essential workforce</a> to learn about what workers and sectors are included. </div>
```

## Hidden keywords

Add hidden keywords when you’d like a page or quick answer to appear in searches for a keyword, but cannot work that keyword into the visible text. The keyword below is hidden in the answer part of a quick answer.

```
<div style="display:none;" class="wp-accordion-content"><!-- county map --></div>
```
