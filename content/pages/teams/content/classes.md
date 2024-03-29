---
title: Classes
date: Last Modified 
permalink: /teams/content/classes.html
eleventyNavigation:
  key: Classes
  parent: Editing
  order: 216
---

Here are some CSS classes that are used often on our website. They are added in WordPress via a block’s **Advanced** drop-down.

* [Accordions](#accordions)
* [Emphasized text](#emphasized-text)
* [Small text](#small-text)
* [Make a heading appear larger](#make-a-heading-appear-larger)

## Accordions

An accordion is a box that contains header text and a plus button (+). Clicking the plus button expands the box to display more text. To make an accordion, use classes.

### Title box

Create the title and expandable box with the class **wp-accordion**. Use a header block for the accordion title and apply this class to it.

![Block section in WordPress with accordion class](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/wp-accordion.png)

This class makes the content look like this:

![Questions accordion](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/questions.png)

### Body

To create the body that appears when the title is opened, use **wp-accordion-content** class. 

This class makes the content look like this:

![Opened accordion with answer](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/answers.png)

The class must be added individually to each content block in the body, whether it’s a paragraph or a list. In the example above, each of the 4 paragraphs had the class added.

Once marked with this class, each block is assumed to be part of the answer to the *wp-accordion* before it. There is no limit to how many *wp-accordion-content* blocks a question can have.

### Troubleshooting

* If body text appears outside the accordion, check to see if it’s missing a class.
* Class tags will often fall off a block if it’s copied and pasted from one place on the page to another.

## Emphasized text

To make text larger, use the emphasized CSS class. You can add it in the right menu.

![Block section in WordPress with emphasized text class](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/emphasized.png)

Only use emphasized text for the first block of text in the page, after the page title and before the page index. Keep this to one or two brief sentences. They should give the most important idea on the page, or the gist of what the page contains.

## Small text

In our page style, small text is only used rarely. It's the online equivalent of "fine print."

To make text smaller than regular body text, use the **small-text** CSS class. You can add it in the right menu.

![Block section in WordPress with small text class](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/small-text.png)

If hand-coding HTML, you can include it as you would any CSS class.

```
<p class="small-text">Offer valid for free topping, or equivalent side serving, of queso blanco with the purchase of a full-priced entrée item. Limit one free serving per entrée; redemption is subject to availability. Must be ordered with entrée item. Excludes online, mobile, and catering orders. Valid only on June 15, 2021 at participating Chipotle Mexican Grill restaurants in California. May not be combined with other coupons, promotions, or special offers. Void where prohibited; additional restrictions may apply.</p>
```

Here's how that looks when published:

![Small text example](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/small-text-example.png)

## Make a heading appear larger

When does an H3 look like an H2? When you give it an H2 class. This changes the appearance of the header while preserving hierarchy for screen readers.

Simply add the size you’d want your headers to appear as under **Additional CSS classes**. If there is already a class there, just put a space between them.

![Block section in WordPress with header class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/header-class-in-block.jpg)

You can do the same thing by using this code in a **Custom HTML** block or in **Code Editor**:

```
<!-- wp:heading {"level":3,"className":"h2"} -->
<h3 class="h2">Regions</h3>
<!-- /wp:heading -->
```

But use this trick sparingly. Headers really should go down in size as they go down in the hierarchy. Not only does this provide a consistent look-and-feel among pages, it helps our site remain accessible to those who use screen readers. 




