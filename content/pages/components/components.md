---
title: Components
date: Last Modified 
permalink: /components/components.html
eleventyNavigation:
  key: Components
  parent: Components and styles
  order: 53
---

## Simple components and classes

These are components that can be applied by the content team without help from a developer.

### Page index

![Generic example of page index](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/page-index.jpg)

#### When we use it

We use the page index on every page with an introductory sentence to give people a sense of what’s on the page. The anchor links in the index allow people to get to the information they’re looking for, even if the page is long. Learn more about the page index in the [content style guide](https://teamdocs.covid19.ca.gov/components/when/content-style-guide.html#page-indexes).

#### How to apply

* Start with a brief sentence that states the most important takeaway on the page using the emphasized text class.
* Follow with _On this page_: in regular size.
* Make a bulleted, bolded list of the h2 headers on the page. Do not link subheaders. If something is important enough to appear in the page index, elevate it to an h2 header.
* Make each h2 header an anchor link and link each item in the index to its corresponding header.

#### Figma and Storybook documentation

### Highlight box

![Generic example of highlight box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box.jpg)

#### When we use it

Urgent information can be highlighted at the top of a page with a highlight box. It can include a right-aligned image next to body text and an action link (button), or can stand alone without these elements.

Use only one per page and position it at the top. Use it sparingly and get approval before publishing. Highlight boxes are an exception to our page style, not a rule--there should not be one on every page.

#### How to apply

For this highlight box with just text:

![Highlight box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box.jpg)

The code is:

```
<div class="highlight">
<h2 class="h3 color-primary mt-0">Regional Stay Home Order ended January 25, 2021</h3>
<p>Counties returned to their appropriate tier under the Blueprint for a Safer Economy. Other state orders are still in place. See details on the <a href="https://covid19.ca.gov/stay-home-except-for-essential-needs/">About COVID-19 restrictions page</a>.
</p>
</div><p></p>
```

For this highlight box with text and action link:

![Highlight box with action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-button.png)

The code is:

```
<div class="highlight">
<h2 class="h3 color-primary mt-0">Get information on safer school reopening</h3>
<p>If you’re a school leader, staff, or parent, the Safe Schools For All Hub is for you. Get updated information from the Department of Public Health, request technical assistance, or submit your concerns.
</p>
      <a class="button-lightblue font-size-1em" href="https://schools.covid19.ca.gov/">Visit the Safe Schools Hub</a>
</div><p></p>
```

For this highlight box with text, image, and action link:

![Highlight box with image and action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-image.jpg)

The code is:

```
<div class="highlight">
  <div class="row">
    <div class="col-md-9 order-last order-md-1">
      <h2 class="h3 color-primary mt-0">Sign up for COVID-19 vaccine notifications
      </h3>
      <p class="pr-0 pr-md-5">Get notified when it’s your turn to get the COVID-19 vaccine. If you're in Los Angeles or San Diego, you can also schedule your appointment.
      </p>
      <a class="button-lightblue font-size-1em" href="https://myturn.ca.gov/landing">Sign up now</a>
    </div>

    <div class="col-md-3 text-center py-4 p-0 pt-md-0 order-1 order-md-last">
      <a href="https://myturn.ca.gov/landing"><img class="img-fluid" loading="lazy" src="https://files.covid19.ca.gov/img/Vaccinate_ALL_58--en.png" alt="Map of California with text Vaccinate ALL 58 - Together we can end the pandemic." style="width:250px"></a>
    </div>
  </div>
</div>
```

#### Figma and Storybook documentation

### Accordion

#### When we use it

We use accordions in two situations:

* For content in question and answer format
* To group like content together

Content in accordions show up as *quick answers*, which means they can appear in search results on the site.

#### How to apply

To create an accordion, use the *wp-accordion* class to the text that will be the title of the accordion. Always make this content an H4 header.

To include a block inside the accordion, use the *wp-accordion-content* class. This must be applied to every block that you want inside the accordion. Missing a block will end the accordion and hide any blocks with the wp-accordion-content class below that missed block.

#### Figma and Storybook documentation

### Table
#### When  we use it
#### How to apply
#### Figma and Storybook documentation

### Table arrow
#### When we use it
#### How to apply
#### Figma and Storybook documentation

## Complex components and classes (requires dev team)

### Bar link
#### When we use it
#### How to apply
#### Figma and Storybook documentation

### Video component
#### When we use it
#### How to apply
#### Figma and Storybook documentation

### Video play button
#### When we use it
#### How to apply it
#### Figma and Storybook documentation

### Large tab
#### When we use oy
#### How to appl
#### Figma and Storybook documentation

### Small tab
#### When we use it
#### How to apply
#### Figma and Storybook documentation

### Survey banner
#### When we use it
#### How to apply
#### Figma and Storybook documentation
