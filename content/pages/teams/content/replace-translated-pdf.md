---
title: Replace a translated PDF
date: Last Modified 
permalink: /teams/content/replace-translated-pdf.html
eleventyNavigation:
  key: Replace translated PDF
  parent: Uploading
  order: 225
---

To replace a translated PDF, you'll start in Airtable before doing the actual upload through github.

## Airtable

1. Log into [Airtable](https://airtable.com/).
2. Open the **ODI File Tracker** base (purple). 
3. Select the **ODI File Tracker** tab, and the **ODI Publish Files** view. 
4. Scroll to the bottom and select the **+** to create a new row. 
5. In this new row, go to the _ODI Status_ field, select the **+** sign, and select the **10.4 Translated guidance or checklist received** label.
6. In the _Language_ field, select the **+** and then select the label for the language that is being published.
7. In the _ODI industry guidance category key_ field, select the **+** sign, and select the appropriate industry label. 
8. In the _PDF Template_ field, select the **+** and select the **guidance** label.
9. Add the file name and the permalink in the appropriate fields. 
10. Move the finalized guidance PDF that's ready to be published to the [Google Drive Publish](https://drive.google.com/drive/folders/1f8ZjcJcXxFt-he7NT6g3S7uJ69CfpwAz?usp=sharing) folder. This file must be correctly named before moving to the _Publish_ folder. 
12. Once the file is in the Google Drive folder, copy the link to the file and paste it into the _URL google drive location_ field in airtable. 
13. In airtable, add a _Target web publish date_ for this file. 
14. Download the file from Google Drive Publish folder to your computer.

## Github

1. Go to https://github.com/cagov/covid-static.
2. Select the **pdf** folder.
3. In the upper-right corner, select the **Add file** button.
4. Select **Upload files** from the dropdown menu.
5. Upload your file by dragging it into the _Drag files here to add them to your repository_ box or selecting **choose your files** and using the popup window. You can attach multiple files if you want to upload all translated guidances at one time. **Do not upload the EN PDF** as it will replace the currently posted English PDF which may be more recent than the translated pdfs received.
6. In the _Commit changes_ section, enter brief details (less than 50 characters) about what you're doing in the first line that contains the placeholder text _Add files via upload_, e.g., "replacing-translated-guidance-hair-salons-13" with 13 indicating that all 13 translations are being replaced by this upload. This information will be available in the Github history and #code-movement on Slack to identify what changes happened. 
  a. Adding additional details in the larger box with the placeholder text _Add an optional extended description_ is only if you have extended information to add.
7. Select the green **Commit changes** button to submit the PDF for upload.
8. To track the status of the PDF upload, select **Actions** in the menu at the top of the page. The text added in the _Add files via upload_ line from the _Commit changes_ section will be listed here. When a green check mark appears to the left of this text, the PDFs have been uploaded (~1 min). 
9. Copy the URL in github, return to Airtable, and paste the link in the _Github download URL_ field, and also add the commit hash to the _git commit hash_ field. 
10. Select the permalink in Airtable to verify the the file has been uploaded. Make sure the new date is showing on the file at this link. 
11. Add the date and time of publication to the _Date updated web_ field.
12. Return to the _ODI Status_ field, and select the **+ sign** to add the **16 - File published** status.
13. If the translated guidance is one of the 6 languages that are not fully supported on the site (Armenian, Hmong, Khmer, Punjabi, Russian, and Thai), create an issue in Jira to have these URLs added to the _Industry guidance in Other Languages_ page. Once those are added to the site, return to Airtable to document that in the _Internal log_ field.
14. If any metadata issues are identified with the file, use the _Internal log_ field in the Airtable record to document those.
15. If the date on the front page of this translated guidance PDF is not the same as the current English version of this guidance, document that in the Airtable record using the _internal log_ field. 
16. Once you've published all availabe translations for this guidance, check the boxes in the _Notify Labor_ field. 
17. Go to the **PDF Historical Files** base in Airtable (pink). Use the first tab on the left, and the **Grouped by industry category** view. Find all of the translated guidance PDFs for that language that have been uploaded and make sure the box is checked in the _is same as public version in api_ field for the most current file published.
23. Email stakeholders confirming when guidance has been published. 
