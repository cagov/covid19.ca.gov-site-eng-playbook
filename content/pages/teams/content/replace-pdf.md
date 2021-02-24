---
title: Replace a PDF
date: Last Modified 
permalink: /teams/content/replace-pdf.html
eleventyNavigation:
  key: Replace PDF
  parent: Uploading
  order: 224
---

This process includes steps for uploading a PDF to replace an existing version (updating).

Links and notes for pdf publishing (new process with airtable)

## Airtable:
[**ODI File Tracker (Purple)**](https://airtable.com/tblIhJbHhqtWDqJoR/viwUwJHYOsYN4pIyl?blocks=hide)
* Use this to start and track each pdf that is being published. 
* Select tab labeled **ODI file tracker**.

[**PDF Historical (Pink)**](https://airtable.com/tblIhJbHhqtWDqJoR/viwUwJHYOsYN4pIyl?blocks=hide)
* Select tab labeled **Git history, PDF metadata, and active files**.
* Select a view appropriate for what you need (e.g., **Grouped by Industry category key**).

## Google Drive [Publish](https://drive.google.com/drive/u/2/folders/1f8ZjcJcXxFt-he7NT6g3S7uJ69CfpwAz) folder:
* First check that the pdfs appear to have the correct filenames. 
* Put the files you are about to publish in the google drive **Publish** folder. 

## Github [Covid-Static PDF](https://github.com/cagov/covid-static/tree/master/pdf) folder:
* This step will make your file “live” within minutes of upload. Staging first is not available. 
* Make sure you are in the **pdf** folder: https://github.com/cagov/covid-static/tree/master/pdf
* You may need to download the file onto your device to then upload it to covid-static. Dragging and dropping the pdf from Google Drive Publish folder into covid-static pdf folder hasn’t worked for several of us.
* Once the upload to github is complete, make sure to test that it’s working by clicking on the link that you added in the airtable tracker for this file. 
* Once confirmed that it’s live, change the _ODI file status_ to _Publish_ in the [ODI file tracker](https://airtable.com/tblIhJbHhqtWDqJoR/viwUwJHYOsYN4pIyl?blocks=hide) (purple airtable). Then check the [PDF Historical](https://airtable.com/tblIhJbHhqtWDqJoR/viwUwJHYOsYN4pIyl?blocks=hide) (Pink) airtable and verify that your newly uploaded file is there, and the _green check box_ is selected.

## Old process steps below - need to update
1. If you’re uploading an updated version of a PDF, find the current version of your PDF on the live site. Find a difference between the current version and the one you’re uploading so you can confirm the new version uploads later.
  a. A date is usually the most convenient reference to use.
2. Rename the updated PDF so it’s the same as the existing PDF.
  a. The name must be identical.
3. Go to https://github.com/cagov/covid-static.
  a. Select the **pdf** folder.
  b. In the upper-right corner, select the **Add file** button.
  c. Select **Upload files** from the dropdown menu.
  d. Upload your file by dragging it into the _Drag files here to add them to your repository_ box or selecting **choose your files** and using the popup window. 
  e. In the _Commit changes_ section, enter brief details (less than 50 characters) about what you’re doing in the first line that contains the placeholder text _Add files via upload_. This information will be available in the Github history and #code-movement on Slack to identify what changes happened. Use hyphens in place of spaces. This information will be available in the Github history and #code-movement on Slack to identify what changes happened (e.g., “replacing-translated-guidance-agriculture-12”). 
  f. Adding additional details in the larger box with the placeholder text _Add an optional extended description_ is only if you have extended information to add.
  g. Select the green **Commit changes** button to submit the PDF for upload.
  h. To track the status of the PDF upload, select **Actions** in the menu at the top of the page. The text added in the _Add files via upload_ line from the _Commit changes_ section will be listed here. When a green check mark appears to the left of this text, the PDF had been uploaded.
4. Return to the live page and confirm the updated PDF comes up when the link is selected.
  a. It usually takes around 1 minute for PDFs to push to the live site.
  b. If it doesn’t come up, confirm in #code-movement that the PDF went through. If it did, confirm the filename of the PDF was the same.
5. Open the Translations Tracking Sheet in Google Drive.
6. Confirm the PDF is listed in the **Guidance Pdfs** tab (or the Checklists tab) with the link. 
7. Select the **Metadata** tab (for either guidance or checklists). Use this tab to note if there is an issue with the PDF metadata, e.g., Retail Checklist label shows “Schools guidance.”
8. Select the **Dates** tab (either guidance dates or checklist dates), and enter the new date of the PDF. 
