---
title: Classes
date: Last Modified 
permalink: /teams/content/classes.html
eleventyNavigation:
  key: Classes
  parent: Editing
  order: 216
---

Here are some CSS classes that are used often on our website. They are added in WordPress via a Block’s **Advanced** drop-down.

* Accordions
* Emphasized text
* Make a heading appear larger

## Accordions

All the questions and answers on our site are contained within collapsible accordions. To make accordions, you use classes.

### Questions

Questions get the class *wp-accordion*.

IMAGE

This class makes the question look like this:

IMAGE

### Answers

The answers that follow the question get the *wp-accordion-content* class. 

This class makes the answer look like this:

IMAGE

The class must be added individually to each content block in the answer, whether it’s a paragraph or a list. In the example above, each of the 4 paragraphs had the class added.

Once marked with this class, each block is assumed to be part of the answer to the *wp-accordion* before it. There is no limit to how many *wp-accordion-content* blocks a question can have.

### Troubleshooting

* If answer text appears outside the accordion, check to see if it’s missing a class.
* Class tags will often fall off a block if it’s copied and pasted from one place on the page to another.

## Emphasized text

To make text larger, use the emphasized CSS class. You can add it in the right menu.

IMAGE

In our page style, emphasized text is only used for the first block of text in the page, after the page title and before the page index. Keep this emphasized text to one or two brief sentences. They should give the most important idea on the page, or the gist of what the page contains.

## Make a heading appear larger

When does an H3 look like an H2? When you give it an H2 class. This changes the appearance of the header while preserving hierarchy.

Simply add the size you’d want your headers to appear as under **Additional CSS classes**. If there is already a class there, just put a space between them.

![Block section in WordPress with header class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/header-class-in-block.jpg)

You can do the same thing by using this code in a **Custom HTML** block or in **Code Editor**:

```
<!-- wp:heading {"level":3,"className":"h2"} -->
<h3 class="h2">Regions</h3>
<!-- /wp:heading -->
```

But use this trick sparingly. Headers really should go down in size as they go down in the hierarchy. Not only does this provide a consistent look-and-feel among pages, it helps our site remain accessible to those who use screen readers. 



