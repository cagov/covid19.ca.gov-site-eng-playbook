---
title: Upload or replace an image
date: Last Modified 
permalink: /teams/content/upload-image.html
eleventyNavigation:
  key: Images
  parent: Uploading
  order: 223
---

We host images through GitHub. This gives us a version history if the image changes over time.

1. Optimize the image using an image optimizer like [Squoosh](https://squoosh.app/).
  a. Smaller images load more easily on lower-performance devices. Keeping images easy to load is part of our commitment to accessibility.
  b. Reduce the image’s file size to under 500KB.
3. Give the image a descriptive name so it's easy to find. Use hyphens between words.
  a. For example, if the image is a .jpg file of a woman wearing the mask, use the name _woman-wearing-mask.jpg_.
3. If you're uploading a new version of an image:
  a. Find the current version of your image on the live site. Find a difference between the current version and the one you're uploading (like name or file size) so you can confirm the new version uploads.
  b. Rename the updated image so it's exactly the same as the existing image. The new image will then replace the older image.
4. Go to https://github.com/cagov/covid-static/tree/master/img.
  a. In the upper-right corner, select the **Add file** button.
  b. Select **Upload files** from the dropdown menu.
  c. Upload your file by dragging it into the _Drag files here to add them to your repository_ box or selecting **choose your files** and using the popup window. 
  d. In the _Commit changes_ section, enter brief details (less than 50 characters) about what you're doing in the first line that contains the placeholder text _Add files via upload_. This information will be available in the Github history and #code-movement on Slack to identify what changes happened. 
  e. If you have more details to add, use the larger box with the placeholder text _Add an optional extended description_.
  f. Select the green **Commit changes** button to upload the image.
  h. To track the status of the upload, select **Actions** in the menu at the top of the page. The text added in the _Add files via upload_ line from the _Commit changes_ section will be listed here. When a green check mark appears to the left of this text, the image has been uploaded.
5. Once the upload is finished, the file will be available at the URL files.covid19.ca.gov/img/ followed by the file name, including the file extension. There may be a brief delay before it appears.
6. If you updated an image, return to the live page and confirm the updated image is showing.
  a. It usually takes around 1 minute for an image to push to the live site.
  b. If it doesn't come up, confirm in #code-movement that the image went through. If it did, check that the filename of the image was the same.

## Translated images

If you have an image with text in different languages, you can upload it so it's displayed automatically on the corresponding translation of the page. 

Use the same language-specific suffix that is used for PDFs (for example, _–es_ for Spanish). If there is not a language-specific image, the site will default to the English version.

For this process to trigger, the English version of the image must have the _–en_ suffix.

Use the regular upload process to add your translated image with the appropriate suffix.
