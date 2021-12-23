---
title: Using images
date: Last Modified 
permalink: /teams/content/images.html
eleventyNavigation:
  key: Using images
  parent: Editing
  order: 213
---

When using images in page content, stick to certain standards to maintain a consistent look and feel sitewide. We consider:

* [When to use images](#-when-to-use-images)
* [Image use rights](#image-use-rights)
* [Aesthetics and style](#aesthetics-and-style)
* [When to use captions](#when-to-use-captions)
* [Size and resolution](#size-and-resolution)

You'll need to know how to:

* [Add an image](#adding-an-image)
* [Add alt text for accessibility](#adding-alt-text-for-accessibility)
* [Center an image](#centering-an-image)
* [Add a caption to an image](#adding-a-caption)
* [Align an image to the right or left of text](#aligning-an-image-to-the-right-or-left-of-text)
* [Add a caption to an image aligned right or left](#adding-a-caption-to-an-image-aligned-right-or-left)

## When to use images

Images can add life, spark interest, and give context to text content.

Use images sparingly. Too many images can be visually distracting. Image files also increase page load times for mobile users and those with low bandwidth.

## Image use rights

Respect copyrights. Only use images you know you have the right to use. This includes:

* Photos you took yourself, or someone took for you
* Graphics created for you by a designer
* Images you paid royalties to use
* Royalty-free images

If you do not know the source of an image, don’t use it. All images are copyrighted by their owner when created.

## Aesthetics and style

For photos, we recommend the image be the full width of the page, be centered, and have a 5x3 aspect ratio.

Illustrations/graphics should be inline (to the right or left of text) or centered. Centered images should be full width, but inline images can be smaller.

## When to use captions

Captions are optional. Use a caption when you want to add context to the image or make a point that the image illustrates. They can also be used for image attribution or copyright.

Keep your captions brief. They are usually in smaller italics text, which is harder to read.

Captions should not be a description of the image for those who use screen readers. That is handled by alt text.

## Size and resolution

Resize and compress your images if needed with tools like Squoosh or Photoshop.

### File size and resolution

The file size should be as small as possible without looking like quality is being lost. Anything less than 500KB in size is OK.

### Dimensions

Images that are the full width of the page should be 920 pixels wide in a landscape orientation. They will automatically resize to 325 pixels when viewed on a mobile device.

* Desktop width: 920px
* Mobile width: 325px

Images that are inline to the right or left of text can be smaller, and either portrait or landscape. Make sure they aren’t so long they cause a lot of whitespace.

## Adding an image

Upload your image to Github:

1. Go to https://github.com/cagov/covid-static/tree/master/img (requires access).
2. Click **Add files** > **Upload file**.
3. Drag and drop your file into the field or choose file from computer.
4. Select **Commit changes**.
5. To see uploading status, to go the **Actions** tab.
6. The URL for the image is https://files.covid19.ca.gov/img/ + filename.

To add an image to page or post in WordPress:

1. Open the page or post.
2. Add the image block where you want the image.
3. Select **Insert from URL**.
4. Paste or type URL.
5. Select **Update** to publish.

## Adding alt text for accessibility

Alt text helps people that use screen readers by reading out a description of an image. It increases a website’s accessibility and SEO ranking.

All images used in a web page should get alt text. The only exceptions are images that are purely decorative, like those used for bullet points.

To add alt text:

1. Select the image in the WordPress page or post.
2. In the right _Block_ menu, find _Image settings_ > _Alt text_.
3. Paste the text you’ve written in that field.
4. Select **Update** to publish.

Consult [How To: Write Good Alt Text](https://supercooldesign.co.uk/blog/how-to-write-good-alt-text) for tips on writing useful descriptions.

## Centering an image

WordPress offers a way to center an image, but it does not work. Instead, convert your block to **Custom HTML** and add this div code around your image:
  
```
  <div class="text-center">
<img src="..." alt="...">
</div>
```

## Adding a caption

If you want to caption an image, use a Custom HTML block to insert a paragraph with the "caption" class after the code for that image. This will give your caption text the standard styling, which is small text, italicized, with left alignment.

Because you used this class, if caption style changes later, you will get the new styling without having to make any changes.

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
  </div>
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

### Image dimensions

* Desktop width: 920px
* Mobile width: 325px

### Making an image responsive

* Use the ["picture"](https://webdesign.tutsplus.com/tutorials/quick-tip-how-to-use-html5-picture-for-responsive-images--cms-21015) tag. This needs a fallback for Internet Explorer, but the format accepts multiple sizes.
* Bootstrap’s [.img-fluid tag reference](https://getbootstrap.com/docs/4.0/content/images/)
