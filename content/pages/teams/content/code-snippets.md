---
title: Code snippets
date: Last Modified 
permalink: /teams/content/code-snippets.html
eleventyNavigation:
  key: Code snippets
  parent: Editing
  order: 215
---

Below are examples of code you can use in WordPress posts. HTML can be inserted using a **Custom HTML** block. CSS classes can be added via a Block’s **Advanced** drop-down when they apply to a whole block, or inserted into an HTML tag when they don't.

* Hidden question & answer
* Hidden keywords
* Action link
* External link icon
* PDF link icon
* Highlight box
* Making a header larger while preserving hierarchy
* Centering an image
* Adding a caption to an image - COMING SOON
* Aligning an image to the right or left of text
* Adding a caption to an image aligned right or left - COMING SOON
* Moving arrow button
* Emphasized text
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

## Action link

An action link is styled as a button so it stands out. It is used for a high-priority link near the top of the page. Only use one action link per page. Using a leading icon is preferred, but optional. Always put a space after the icon.

For this action link:

![Action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/action-link.jpg)

The code is:

```
<a class="action-link" href="https://covid19.ca.gov/sign-up-for-county-alerts/"><span class="ca-gov-icon-warning-circle"></span><strong> Sign up for county alerts</strong></a>
```

## External link icon

Use an external link icon to tell people a link will take them away from covid19.ca.gov. This includes any sites that use a domain that includes covid19.ca.gov, but is not maintained by our team. It’s OK to use this formatting multiple times if there are multiple external links in one paragraph.

For this external link icon:

![External link icon](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/external-link.png)

The code is:

```
<p>After reading, you can request to <a class="external" href="https://state-of-california-agency.forms.fm/great-plates-delivered-food-provider-interest-form">volunteer or provide meals</a>.</p>
```
## PDF link icon

Use a PDF link icon to tell people a link will take them to a PDF. Use this formatting on any link to a PDF document, regardless of who owns it. It’s OK to use this formatting multiple times if there are multiple external links in one paragraph.

For this PDF link icon:

![PDF link icon](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/pdf-link-icon.png)

The code is:

```
<p>More details about receiving meals are available in the <a class="pdf" href="https://files.covid19.ca.gov/pdf/great-plates-delivered-participants-faqs.pdf">participant FAQ</a>.</p>
```

## Highlight box

Urgent information can be highlighted at the top of a page with a highlight box. It can include a right-aligned image next to body text and an action link (button), or can stand alone without these elements.

Use only one per page and position it at the top. Use it sparingly and get approval before publishing. Highlight boxes are an exception to our page style, not a rule--there should not be one on every page.

For this highlight box with just text:

![Highlight box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box.jpg)

The code is:

```
<div class="highlight">
<h3 class="color-primary mt-0">Regional Stay Home Order ended January 25, 2021</h3>
<p>Counties returned to their appropriate tier under the Blueprint for a Safer Economy. Other state orders are still in place. See details on the <a href="https://covid19.ca.gov/stay-home-except-for-essential-needs/">About COVID-19 restrictions page</a>.
</p>
</div><p></p>
```

For this highlight box with text and action link:

![Highlight box with action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-button.png)

The code is:

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

The code is:

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

Insert it using Code Editor. Use this occasionally and in consultation with the Design team. Headers should go down in size as they go down in the hierarchy. 

If you’d like to do this same thing without writing custom code, add the size you’d want your headers to appear as under Additional CSS classes. If there is already a class there, put a space between them.

![Block section in WordPress with header class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/header-class-in-block.jpg)

## Centering an image

WordPress offers a way to center an image, but it does not work. Instead, convert your block to **Custom HTML** and add this div code around your image:
  
```
  <div class="text-center">
<img src="..." alt="...">
</div>
```
## Adding a caption to an image

(In development.)

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

## Adding a caption to an image aligned right or left

To have an image with a wrapping caption to the left or right of the text, use a Custom HTML block with 2 columns such as col-md-8. Number 8 means that this column will occupy 8 out of 12 grid columns (or 2/3 of the page width). If the first column has a number 8 in it, that means that second column for the image needs to have a number 4, or col-md-4 (because 8 + 4 = 12). In the image columns right under the image, you can insert the paragraph text with class "caption".

```
<p class="caption">Caption text</p>
```

So for this alignment:

![Right-aligned image with caption](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/caption-aligned-right.png)

Use this code:

```
<div class="container py-4">
    <div class="row">
      <div class="col-md-8">
        <p><strong>Contact tracing works when you answer the call or text.</strong></p><p>All you have to do is answer the phone call or respond to the text message survey sent by your local health department.</p>
  <p>Contact tracing is an anonymous way to do your part. The more people answer the call or text, the more lives and jobs California will save and the faster we can re-open schools and businesses and keep them open. Your information is always kept confidential.
  </p>
      </div>
  <div class="col-md-4">
        <img src="https://files.covid19.ca.gov/img/Asset4at2x1.png" alt="illustration of man on phone" style="width: 250px;">
      
    <p class="caption">Image caption could be really long. And if the caption is longer than this one, it pushes the image and body text within that paragraph weirdly left, creating empty space on the right.</p>
<p class="caption">We'd like the caption text to be smaller, italicized, and wrap under the image without creating empty space. </p>
    </div>
    </div>
  </div>
```

## Moving arrow button link

This code makes a special navigation link that responds to hover-overs with motion and a color change. Use this only once per page.

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
</div>
```

There are many standard color combinations for this button. See the [Examples](https://staging.covid19.ca.gov/sample) page for a preview, and check its [Wordpress file](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=6854&action=edit) for the code for each.

## Emphasized text

To make text larger (like for the first sentence of a page when implementing the page index), use the _emphasized_ CSS class. You can add it in the right menu.

![Block section in WordPress with emphasized class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/emphasized-class-in-block.jpg)

## Titles in links

If you use the same hyperlink text with different URLs on a page, this will trigger an accessibility flag in SiteImprove. Try to reword the text to reflect the different URLs. If you cannot, use a title with the link. This signals to screen readers that the link is different.

To add a title, make a link like usual. When finished, view that section in _Code editor_ and add the code beginning **title**, as shown below.

```
<a href="https://covid19.ca.gov" title="[the text you’d like the screen reader to read instead of the hyperlink text on the screen]">[hyperlink text]</a>
```
