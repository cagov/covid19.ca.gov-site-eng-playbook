---
title: Adding PDFs to the Industry guidance in other languages page
date: Last Modified 
permalink: /teams/content/ig-other-languages.html
eleventyNavigation:
  key: IG in other languages
  parent: Uploading
  order: 226
---

There are 6 languages that we have some guidance PDFs for, but which are not supported by a sitewide translation. They are Armenian, Hmong, Khmer, Punjabi, Russian, and Thai. We publish documents in those languages on a page called [Industry guidance in other languages](https://covid19.ca.gov/guidance-languages/). 

In general, PDFs should already have been uploaded, their URLs created and logged, and the new content added to a Jira ticket. 

If they were not, follow the instructions for [Replacing translated guidance PDFs](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/teams/content/replace-translated-pdf.html) to do so.

Then you’re ready to add PDFs to this page, with link titles in the native language:

1. In WordPress, find the post **Industry guidance in other languages (links fragment)** and select **Edit**.
2. Find the language you’re working in, and scroll to the bottom of that list.
3. In the Jira ticket, select the link to the PDF you’d like to add so it opens in your browser.
4. Select the title from the first page of the PDF and copy (**Ctrl+C**).
5. Open a new page in a word processing program. Microsoft Word works well. Do not use Notepad, as it does not support all the needed alphabets.
6. Paste the title into your doc (**Ctrl+V**).
7. Go back to your browser and copy the URL to the PDF (**Ctrl+C**).
8. In your doc, select all (**Ctrl+A**).
9. Right-click on the selected text and choose **Link**.
10. Paste the URL in the link box.
11. Select all again (**Ctrl+A**) and cut (**Ctrl+X**).
12. Go to the WordPress post, make a new bullet item at the bottom of the list, and paste your link there.
13. Keep doing steps 1-12 until all the PDFs for that language have been linked in the post.
14. When you’re finished with a language, select **Update** so it publishes. (If you close the browser window without updating your changes, they will be lost.)
15. Make any necessary notes in the comments of the Jira ticket, and mark it as **Done**.

## Housekeeping items

If you upload new guidance PDFs, 
* Add their URLs to a Jira ticket, noting the language and subject of each PDF
* Assign the ticket to the responsible content captain so they know to update the page.
