---
title: Using images
date: Last Modified 
permalink: /teams/content/images.html
eleventyNavigation:
  key: Using images
  parent: Editing
  order: 213
---

When using images in page content, it's important to stick to certain standards to maintain a consistent look and feel sitewide. We consider:

* Aesthetics and style
* When to use images
* Writing captions
* How to add images
* Size and resolution
* HTML for responsive images

It's also important to know how to:

* Center an image
* Add a caption to an image
* Align an image to the right or left of text
* Add a caption to an image aligned right or left

## Aesthetics and style

* For photos, the design team recommends image be the full width of the page, be centered, and have a 5x3 aspect ratio.
* Illustrations/graphics should be inline (to the right or left of text) or centered. Centered images should be full width, but inline images can be smaller.

## When to use images

(When/why to use photos)

## Writing captions

(Advice on writing captions)

## How to add images

* Resize and compress with Squoosh.com (or other tool of choice)
* Upload to Github
* Add to page in WordPress
* Use classes in WordPress to define desktop and mobile images

## Size and resolution concerns 

(Including accessibility through performance)

### Filesize

The file size should be as small as possible without looking like quality is being lost. Anything less than 500KB in size is OK. 

## Center an image

WordPress offers a way to center an image, but it does not work. Instead, convert your block to **Custom HTML** and add this div code around your image:
  
```
  <div class="text-center">
<img src="..." alt="...">
</div>
```
## Add a caption to an image

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

## Align an image to the right or left of text

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
  </div>
```

## Add a caption to an image aligned right or left

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


### Image dimensions

* Desktop width: 920px
* Mobile width: 325px

## HTML options for sharing responsive images

* Use the ["picture"](https://webdesign.tutsplus.com/tutorials/quick-tip-how-to-use-html5-picture-for-responsive-images--cms-21015) tag. This needs a fallback for IE, but the format accepts multiple sizes.
* Bootstrap’s [.img-fluid tag reference](https://getbootstrap.com/docs/4.0/content/images/)
