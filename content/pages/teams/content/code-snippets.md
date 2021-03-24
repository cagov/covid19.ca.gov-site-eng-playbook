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
* Making a header larger while preserving hierarchy
* Centering an image
* Adding a caption to an image - COMING SOON
* Aligning an image to the right or left of text
* Adding a caption to an image aligned right or left - COMING SOON
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
<h3 class="h2">Regions</h3>
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

If you want to caption an image, use a Custom HTML block to insert a paragraph with the "caption" class after the code for that image. This will give your caption text the standard styling, which is small text, italicized, with left alignment. Even better, if caption style changes later, then by using this class you will get the new styling without having to make any changes.

For this caption:

![Default image with caption](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/caption.png)

The code is this:

```
<div>
<img src="https://files.covid19.ca.gov/img/Women-getting-vaccinated.png" alt="Illustration of a women getting tape on vaccination site" style="width: 920px;">
      
<p class="caption">Every Californian 16 and up will have access to vaccines this spring</p>
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

## Titles in links

If you use the same hyperlink text with different URLs on a page, this will trigger an accessibility flag in SiteImprove. Try to reword the text to reflect the different URLs. If you cannot, use a title with the link. This signals to screen readers that the link is different.

To add a title, make a link like usual. When finished, view that section in _Code editor_ and add the code beginning **title**, as shown below.

```
<a href="https://covid19.ca.gov" title="[the text you’d like the screen reader to read instead of the hyperlink text on the screen]">[hyperlink text]</a>
```
