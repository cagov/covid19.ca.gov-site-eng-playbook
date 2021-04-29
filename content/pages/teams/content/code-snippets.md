---
title: Code snippets
date: Last Modified 
permalink: /teams/content/code-snippets.html
eleventyNavigation:
  key: Code snippets
  parent: Editing
  order: 215
---

Below are examples of code you can use in WordPress posts. HTML can be inserted using a **Custom HTML** block. CSS classes can be added via a Block’s **Advanced** drop-down when they apply to a whole block, or inserted into an HTML tag when they do not. If you're looking for something that is not listed here, check the [components](https://teamdocs.covid19.ca.gov/components/) section of this site.

* Hidden question & answer
* Hidden keywords
* Titles in links

## Hidden question & answer

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

## Titles in links

If you use the same hyperlink text with different URLs on a page, this will trigger an accessibility flag in SiteImprove. Try to reword the text to reflect the different URLs. If you cannot, use a title with the link. This signals to screen readers that the link is different.

To add a title, make a link like usual. When finished, view that section in _Code editor_ and add the code beginning **title**, as shown below.

```
<a href="https://covid19.ca.gov" title="[the text you’d like the screen reader to read instead of the hyperlink text on the screen]">[hyperlink text]</a>
```
