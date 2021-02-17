---
title: Replace a translated PDF
date: Last Modified 
permalink: /teams/content/replace-translated-pdf.html
eleventyNavigation:
  key: Replace translated PDF
  parent: Uploading
  order: 225
---

1. Log into airtable.com.
2. Open the ODI File Tracker base (purple). 
3. Select the ODI File Tracker tab, and the ODI Publish Files view. 
4. Scroll to the bottom and click the + to create a new row. 
5. In this new row, go to the ODI Status field, click on the + sign, and select the "10.4 Translated guidance or checklist received" label.
6. In the Language field, click on the + and then select the label for the language that is being published.
7. In the ODI industry guidance category key field, click on the + sign, and then select the appropriate industry label. 
8. In the PDF Template field, click on the + and select the "guidance" label.
9. Add the filename and the permalink in the appropriate fields. 
10. Move the finalized guidance pdf that is ready to be published to the Google Drive Publish folder: https://drive.google.com/drive/folders/1f8ZjcJcXxFt-he7NT6g3S7uJ69CfpwAz?usp=sharing. This file must be correctly named before moving to the Publish folder. 
12. Once the file is in the google drive folder, copy the link to the file and paste it into the "URL google drive location" field in airtable. 
13. In airtable, add a "Target web publish date" for this file. 
14. Download the file from Google Drive Publish folder to your computer. 
15. Go to https://github.com/cagov/covid-static.
16. Select the **pdf** folder.
17. In the upper-right corner, select the **Add file** button.
18. Select **Upload files** from the dropdown menu.
19. Upload your file by dragging it into the _Drag files here to add them to your repositor_y box or selecting **choose your files** and using the popup window. You can attach multiple files. **Do not upload the EN PDF** as it will replace the currently posted English PDF which may be more recent than the translated pdfs received.
20. In the _Commit changes_ section, enter brief details (less than 50 characters) about what you're doing in the first line that contains the placeholder text _Add files via upload_. This information will be available in the Github history and #code-movement on Slack to identify what changes happened. 
  a. Adding additional details in the larger box with the placeholder text _Add an optional extended description_ is only if you have extended information to add.
12. Select the green **Commit changes** button to submit the PDF for upload.
13. To track the status of the PDF upload, select **Actions** in the menu at the top of the page. The text added in the _Add files via upload_ line from the _Commit changes_ section will be listed here. When a green check mark appears to the left of this text, the PDFs have been uploaded (~1 min). 
14. Copy the url in github, return to airtable, and paste the link in the "Github download URL" field, and also add the commit hash to the "git commit hash" field. 
15. Click on the permalink in airtable to verify the the file has been uploaded. Make sure the new date is showing on the file at this link. 
16. Add the date and time of publication to the "Date updated web" field.
17. Return to the ODI Status field, and click the + sign to add the "16 - File published" status.
18. If the translated guidance is one of the 6 languages that are not fully supported on the site (Armenian, Hmong, Khmer, Punjabi, Russian, and Thai), create an issue in Jira to have these URLs added to the "Industry guidance in Other Languages" page. Once those are added to the site, return to airtable to document that in the "Internal log" field.
19. If any metadata issues are identified with the file, use the "Internal log" field in the airtable record to document those.
20. If the date on the front page of this translated guidance pdf is not the same as the current English version of this guidance, document that in the airtable record using the "internal log" field. 
21. Once you've published all availabe translations for this guidance, check the boxes in the "Notify Labor" field. 
22. Go to the PDF Historical Files base in airtable (pink). Use the first tab on the left, and the "Grouped by industry category" view. Find all of the translated guidance pdfs for that language that have been uploaded, and make sure the box is checked in the "is same as public version in api" field for the most current file published.
23. Email stakeholders confirming when guidance has been published. 
