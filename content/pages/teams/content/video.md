---
title: Video section
date: Last Modified 
permalink: /teams/content/video.html
eleventyNavigation:
  key: Video
  parent: Homepage
  order: 245
---

The video section of the homepage is updated through the [Video Section](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=7482&action=edit) WordPress post.

## What you need to update

To update a PSA video, you'll need:

* The YouTube link to the video you want to feature
* Approvals from the Office of the Governor for the video to feature, title, and video description. Talk with a product lead to get this approval.
* A high-res image still from the video 
  * Enter the YouTube link at https://www.youtubescreenshot.com.
  * Right-click and save the main image it generates.
  * [Upload the image](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/teams/content/upload-image.html) and get the URL (http://files.covid19.ca.gov/img/ followed by filename.jpg).

To feature a press conference, you'll need:

* The YouTube link to the livestream
* The video description on YouTube for this livestream. This can also come from a news release.
* The time it’s expected to begin. This is often in the news release.

For the Governor's or Secretary's press conferences, the WordPress post already has images and descriptions loaded in. Update the date, time, and description as appropriate.

## How to update

* Choose whether you want to feature a PSA video (first row), Governor’s press conference (second row), or secretary’s press conference (third row).
  * Put **yes** in the _Active_ column for video you want to feature, **no** in the other rows.
* Change the _Video Title_.
  * For PSA, this is the title it has in YouTube.
  * For press conferences, update the date and time it’s going live.
* Change the _Description_.
  * For PSA, this is the description it has in YouTube, approved by the Office of the Governor.
  * For press conferences, use the existing description or the YouTube description if it mentions a specific topic.
* Change the _Video URL_, _Video ID_ (last part of the YouTube URL), and (if needed) _Image URL_.
  * [Governor’s YouTube channel](https://www.youtube.com/channel/UCrHSYLKqmLunBzlSfunGDSA)
  * [California Department of Health and Human Services YouTube channel](https://www.youtube.com/channel/UCFvH-hGEKg2elZ7k-_5eQEg)
* For PSA, change the _Image Alt Text_ (use the title of video or another helpful descriptor).
* Do not change the _ButtonText_ (call to action) or _ButtonURL_ (CTA destination).
* Add the **staging-only** tag and select **Update** to stage.
* If all looks well on staging, remove the **staging-only** tag and select **Update** to publish.

## Text and link defaults

These are approved by the Office of the Governor, so do not deviate from them without checking with a product lead first.

### PSA

* Video Title: [Title of video]
* Description: [YouTube description, modified if needed]
* ImageALT: [Title of video]
* ButtonText: More video messages
* ButtonURL: toolkit.covid19.ca.gov

### Governor's press conference

* Video Title: Live at [9:30 AM]: Press conference with the Governor
* Description: Gov. Gavin Newsom addresses California's response to COVID-19.
* ImageALT: Press conference with CA Gov. Gavin Newsom
* ButtonText: See past press conferences
* ButtonURL: www.youtube.com/playlist?list=PLS1sIrqLVSo9jz15dkLRKxOMUR2-MtoH7 

### Secretary's press conference

* Video Title: Live at [12:00 PM]: Press conference with Dr. Mark Ghaly
* Description: CHHS Secretary Dr. Mark Ghaly addresses California's response to COVID-19.
* ImageALT: Press conference with CA CHHS Secretary Dr. Mark Ghaly
* ButtonText: See past press conferences
* ButtonURL: www.youtube.com/playlist?list=PLZqpl41f-8c_DHaRyq9LCD5vHqT-CMkgA 
