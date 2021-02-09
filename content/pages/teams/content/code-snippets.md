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
<div style="display:none;" class="wp-accordion-content"><!-- county map --></div>
```

## Action link

An action link has special styling to help it stand out. It is used for a high-priority link near the top of the page. Use only one action link per page. Using a leading icon is preferred, but optional. Always put a space after the icon.

For this action link:

![Action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/action-link.jpg)

The code is this:

```
<a class="action-link" href="https://covid19.ca.gov/sign-up-for-county-alerts/"><span class="ca-gov-icon-warning-circle"></span><strong> Sign up for county alerts</strong></a>
```

## Highlight box

Urgent information can be highlighted at the top of a page with a highlight box. It can include a right-aligned image next to body text and an action link (button), or can stand alone without these elements.

Highlight boxes now take the place of yellow alert boxes. Use only one per page, and position at the top. Use sparingly, and get approval before publishing. Highlight boxes are an exception to page style, not a rule--there should not be one on every page.

For this highlight box with just text:

![Highlight box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box.jpg)

The code is this:

```
<div class="highlight">
<h3 class="color-primary mt-0">Regional Stay Home Order ended January 25, 2021</h3>
<p>Counties returned to their appropriate tier under the Blueprint for a Safer Economy. Other state orders are still in place. See details on the <a href="https://covid19.ca.gov/stay-home-except-for-essential-needs/">About COVID-19 restrictions page</a>.
</p>
</div><p></p>
```

For this highlight box with text and action link:

![Highlight box with action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-button.png)

The code is this:

```
<div class="highlight">
<h3 class="color-primary mt-0">Get information on safer school reopening</h3>
<p>If you’re a school leader, staff, or parent, the Safe Schools For All Hub is for you. Get updated information from the Department of Public Health, request technical assistance, or submit your concerns.
</p>
      <a class="button-lightblue font-size-1em" href="https://schools.covid19.ca.gov/">Visit the Safe Schools Hub</a>
</div><p></p>
```

For this highlight box with text, image, and action link:

![Highlight box with image and action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-image.jpg)

The code is this:

```
<div class="highlight">
  <div class="row">
    <div class="col-md-9 order-last order-md-1">
      <h3 class="color-primary mt-0">Sign up for COVID-19 vaccine notifications
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

### Yellow alert box - DEPRECATED

**We now use the highlight box instead of a yellow alert box. This code is being kept in case it's needed later.**

Urgent information can be highlighted in a yellow alert box at the top of a page. Use sparingly, and get approval before adding an alert box to a page. 

For this yellow alert box:

![Yellow alert box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/yellow-alert-box.jpg)

The code is this:

```
<div class="alert alert-warning" role="alert"><h4 class="alert-heading">New limited stay at home order</h4><p>COVID-19 is increasing at alarming rates in California and we all need to do our part to stop the surge. As of November 19, 2020, it is required that all non-essential work and activities stop between 10PM and 5AM in counties in the Widespread (purple) tier. Read more in the <a href="https://www.cdph.ca.gov/Programs/CID/DCDC/Pages/COVID-19/limited-stay-at-home-order.aspx" class="alert-link">limited stay at home order</a>.</p></div>
```

## Make a heading larger while preserving hierarchy

When does an H3 look like an H2? When you use this code:

```
<!-- wp:heading {"level":3,"className":"h2"} -->
<h3 class="h2" >Regions</h3>
<!-- /wp:heading -->
```

This is WordPress code you can insert using Code Editor. But don’t go crazy - headers really should go down in size as they go down in the hierarchy. 

If you’d like to do this same thing without writing custom code, simply add the size you’d want your headers to appear as under Additional CSS classes. If there is already a class there, simply put a space between them.

![Block section in WordPress with header class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/header-class-in-block.jpg)

## Centering an image

WordPress offers a way to center an image, but it doesn’t work. So instead, convert your block to Custom HTML and add this div code around your image:
  
  ```
  <div class="text-center">
<img src="..." alt="...">
</div>
```

## Aligning an image to the right or left of text

These two code snippets will comfortably place an image to the right or left of text when viewing the page on a desktop computer. When viewing on mobile devices, it will place the image above the text (if left-aligned on desktop) or below the text (if right-aligned on desktop).

### Left-aligned image

For this alignment:

![Left-aligned image](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/left-aligned-image.jpg)

Use this code:

```
<div class="container py-4">
  <div class="row">
    <div class="col-md-auto">
      <img src="https://files.covid19.ca.gov/img/Asset1-1.png" alt="illustration of a contact tracer" style="width: 250px;">
    </div>
    <div class="col">
      <p><strong>Contact tracing is when public health workers identify and notify the people who were exposed to infected people. </strong> They let them know that they've been in <a href="https://www.cdc.gov/coronavirus/2019-ncov/php/contact-tracing/contact-tracing-plan/appendix.html#contact">close contact</a> with an infected person, and what to do next to keep themselves and their loved ones safe. Public health departments have used contact tracing for decades to fight the spread of infectious diseases. </p>
    </div>
  </div>
</div>
```

### Right-aligned image

For this alignment:

![Right-aligned image](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/right-aligned-image.jpg)

Use this code:

```
<div class="container py-4">
  <div class="row">
    <div class="col">
      <p><strong>Contact tracing works when you answer the call or text.</strong></p>
<p>All you have to do is answer the phone call or respond to the text message survey sent by your local health department.</p>
<p>Contact tracing is an anonymous way to do your part. The more people answer the call or text, the more lives and jobs California will save and the faster we can re-open schools and businesses and keep them open. Your information is always kept confidential.
</p>
    </div>
<div class="col-md-auto">
      <img src="https://files.covid19.ca.gov/img/Asset4at2x1.png" alt="illustration of man on phone" style="width: 250px;">
    </div>
  </di
```

## Moving arrow button

This code allows you to make a special navigation link that responds to mouse-overs with motion and a color change. Use this only once per page.

For this arrow:

![Arrow button](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/arrow-button.jpg)

Use this code:

```
<div class="row py-5 text-center">
    <div class="col-md-3 bg-blue py-4">
        <a href="#" class="link-arrow-white">
            <div class="link-arrow-label">Arrow</div>
<cagov-arrow></cagov-arrow>
        </a>
    </div>
```

There are many standard color combinations for this button. See the [Examples](https://staging.covid19.ca.gov/sample) page for a preview, and check its [Wordpress file](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=6854&action=edit) for the code for each.

## Emphasized text

To make text larger (like for the first sentence of a page when implementing the page index), use the _emphasized_ CSS class. You can add it in the right menu.

![Block section in WordPress with emphasized class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/emphasized-class-in-block.jpg)

## ARIA labels

ARIA labels provide alternate hyperlink text that a screen reader will use instead of the hyperlink as written. If you use the same hyperlink text with different URLs on a page, this will trigger an accessibility flag in SiteImprove. If you can’t reword the text to reflect the different URLs, ARIA labels will satisfy SiteImprove.

To create an ARIA label, make a link like usual. View that section in Code editor and add the code beginning **aria-label***, as shown below.

```
<a href="https://covid19.ca.gov" aria-label="[the text you’d like the screen reader to read instead of the hyperlink text on the screen]">[hyperlink text]</a>
```
