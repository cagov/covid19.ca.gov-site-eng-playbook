---
title: Content style guide
date: Last Modified 
permalink: /components/when/content-style-guide.html
eleventyNavigation:
  key: Style guide
  parent: Content
  order: 205
---

We write for all Californians. Our content bridges the gap between Californians and the information and services they need.

## Content principles

covid19.ca.gov follows the [Office of Digital Innovation content design principles](https://docs.google.com/document/d/1orQyak_oQ2dSrDBYCRjauHTIQE51QGE_Cn4TssYrNX0/edit?usp=sharing). We also use the [Office of Digital Innovation word list](https://docs.google.com/document/d/1ALvcGokcsDYpjtTZ94HaOXyNKTDOx2AUPrtAJpZ7iyk/edit?usp=sharing).

## Content about emerging situations

Give people a sense of calm, control, and purpose. Make people feel they have just enough information to act. Give them the most widely-applicable and urgent info. For specific info, link to state agency content.

Get an authoritative state-level response up first. Fight misinformation by providing the truth directly and clearly. When that’s up, focus on questions you imagine people asking.

Ask these questions when writing content:
* Is the state the right authority on this?
* Does another agency (federal, state, or local) have more detailed or current data?
  * If so, link to them.
* If information will change over time, link to where it will be kept up-to-date.
* Does this content reflect what is currently true?
  * Remove things like intentions or hopes.

Assume that everyone’s reading level is a few grades lower due to stress. Readers are juggling lots of new information, disruptions, and distractions.

* Use:
  * Short sentences
  * One or two syllable words. The CDC maintains [a list of everyday words](https://www.cdc.gov/healthcommunication/everydaywords/index.html).
  * Simple sentence structure
  * A clear hierarchy of information
* Do not use special terms. People probably won’t know what they mean.
* Avoid repetition, even when there are slight differences.
* Keep conditional sentences (if/then) to a minimum.

## Structure and formatting
Well-structured content is easy to read and accessible.

### Headings
Clear headings make pages easier to scan and understand.

* Use sentence case. Capitalize the first word and proper nouns. It’s friendlier and helps readers recognize proper nouns.
* Make the name of your page an h1 header. Only use one h1 header per page.
* Use header levels in ascending numerical order. Do not skip steps. It’s OK to repeat header levels.
* Always have at least one line of text between headers.
* Do not use header tags for full sentences or non-header body text.

Check your heading structure in Google Docs. Select **View** and **Show Document Outline** to confirm they nest appropriately.

### Lead class text
Lead class text makes text larger. Use it to explain the service or topic at the top of the page, underneath the h1. Only use one paragraph of lead class text per page. Use `<p class="emphasized">the text you want</p>` in Wordpress to create lead class text.

### Titles
The title appears when you hover over the page tab in a browser. It helps users change between tabs on their browser.

Make the title the page heading followed by a hyphen and the site name. This gives users a full understanding of the page. Here’s an example, including the coding tags: _<title>Content guide - Alpha.CA.gov</title>_

### Page URLs
Use the h1 of the page to create your URL. This helps search engines find the page.

Replace spaces in the title with hyphens so search engines can read them. Delete the conjunctions, prepositions, and articles as long as the URL still keeps the same meaning.
* A page titled _Hire a licensed contractor for home improvements_ would become _/hire-licensed-contractor-home-improvements_.
* Don’t make _Growing up with diabetes_ into _/growing-diabetes_. This has a different meaning.

Use the site map to build the URL. If the licensed contractor page lives under a page called Services, the URL would be: _alpha.ca.gov/services/hire-licensed-contractor-home-improvements_

Any time the site name is spelled out in content, make it a hyperlink to the homepage.

### Bold, italics, underlining
Make important information or keywords users search for bold. We do not use italics for emphasis.

Do not underline content. Web browsers highlight links automatically. Underlining non-link content confuses readers.

### Links and buttons
Use a button with a form or to highlight something the user wants to do. Links are embedded in text instead of standing alone.

* Link to webpages instead of PDFs as much as possible. Webpages are more accessible across devices, more easily searched, and less likely to break.
  * If you must link to a document, make it a PDF if possible. Word documents, Excel sheets, and PowerPoint presentations require software to view them that people may not have.
  * Indicate if the link is going to a file by providing its extension (like DOC or PPT) so people can choose if they want to download it.
  * Use the PDF link class to format links to PDFs.
* Make the link title match the title of the destination page as much as possible. This helps people know they arrived in the right place.
* When creating a button, be short, descriptive, and distinctive.
* Limit number of links so as to make the text more readable. If you have several relevant links, put them in a bulleted list after your main text.
* Have links support comprehension, not disrupt it. Do not link until it's all right to send the user away (after you've conveyed your point).
* Open links in the [the same tab and window](https://www.w3.org/TR/WCAG20-TECHS/G200.html). Only open content in a new tab or window when there's a good reason to do so. Give them [warning](https://www.w3.org/TR/WCAG20-TECHS/G201.html) when a new tab or window will open.
  * See the [examples](https://staging.covid19.ca.gov/sample) page to see what code to use in WordPress to create linked to other sites and PDFs.
* When you end a sentence with a link, do not include the period in the hyperlink.
* Always create dial links for phone numbers. This allows users, especially mobile users, to dial the number with one click. The WordPress format for the link is `tel:123‑456‑7890`, and the HTML is `<a href="tel:123‑456‑7890">123‑456‑7890</a>`.
  * Use non-breaking hyphens when creating these hyperlinks. These allow phone numbers in Arabic translations to work. The hyphens above are non-breaking. To be sure you're using a non-breaking hyphen, you can also use `&#8209;`.

### Notes and disclaimers
When info (especially data in tables or graphs) needs an explanation, follow it with a note to provide clarity. Make the note smaller to signal to the reader that it is secondary info. In WordPress, use this code in the HTML view to create smaller text: `<p class="small-text"> … </p>`

## Content types
Some content comes across better in non-paragraph form. Bullet points, alerts, and info boxes also make pages easier to scan. 

### Bullet points
Use bullet points for a list of items that are related. Only use bullet points if there is more than one item in the list.

Put a period at the end of a bullet point if it’s a full sentence.
* _Ask family and friends for contractors they recommend._
* _Search online and read reviews, but consider the source._
* _For repairs, your homeowners insurance might cover the cost and suggest contractors for you._

Do not add a period if the bullet point is not a full sentence. Capitalize the first word of every bullet point.
_Ask the contractor to share the name of their insurance carrier and copies of both their:_
* _Workers’ compensation insurance_
* _General liability insurance_

Be consistent with whether your bullet points are sentences or not.

### Numbered lists
Use numbered lists when a user needs to do tasks in a certain order, like a process. They’re especially helpful if the steps happen across different agencies. 
* Start each task with a verb.
* Provide a high-level summary in the task. Put smaller details in the Show/Hide text.
* Keep the description short, no more than a few paragraphs.
  * If it cannot be condensed, make a guide instead.
* Give each number an [ARIA label](https://www.a11y-101.com/development/aria-label) so screen readers can read them aloud as step one, step two, and so on.
* Link to content that already exists on an agency website. Do not duplicate it. Prepare users with the information they need before they select the link.

An example of a numbered list is [Hire a licensed contractor for home improvements](https://www.alpha.ca.gov/hire-licensed-contractor-home-improvements/).

### Questions and answers
People often think in terms of a question they have. Creating anticipated questions and providing answers to them is an effective way to meet their needs.

When creating a question and answer section, just call it _Questions and answers_. Don’t add any information like _Questions and answers about financial help_. If questions and answers cluster around certain topics, create subheaders to organize them.

To prevent a question and answer or other accordion from showing up in search results on covid19.ca.gov, add this class to the accordion title block (which will already have the class **wp-accordion**): **js-qa-exclude**

### Guides
A guide is a comprehensive summary of complex information. It usually spans multiple pages. Side navigation lets users move between pages.

An example of a guide is [Apply for unemployment insurance](https://www.alpha.ca.gov/apply-for-unemployment-insurance/).

### Smart answers
A smart answer gives the user an answer that’s specific to their location or situation. Users enter info into one or two form fields.

* Be clear about any limits of the answer.
  * Example: If we can only look up cities in California, share that up front instead of through an error message. 
* Give the button a descriptive term that anticipates the info the user will receive.
  * Example: **Check your water** instead of **Enter**.
* Make error messages proactive instead of assigning blame.
  * Example: _Please enter a city in California_ instead of _You entered a city outside of California_. 

Examples of smart answers are [Find the minimum wage in your city](https://www.alpha.ca.gov/find-minimum-wage-your-city/) and [Check lane closures for your trip](https://www.alpha.ca.gov/check-lane-closures/).

### Guided answers
A guided answer takes users through multiple questions to provide an answer tailored to them. 
* When the questions are on separate pages, a **Next** button is helpful. The final button should convey the outcome, like **Check if you qualify**.
* Give users a way to get back to the previous question. Separate it from the buttons used to answer questions. 

An example of a guided answer is [Check if you can get a discounted phone service](https://www.alpha.ca.gov/check-if-you-can-get-discounted-phone-service/).

### Checklists
Use a checklist when you want a user to be able to select multiple options from a list. Use radio buttons if you only want them to select one option.

### Forms
Forms allow users to enter in their information and get an answer specific to them and their needs.

* Create titles for each field. Do not use placeholder text that disappears when the user starts typing. It’s hard to remember what belongs in the field or ensure it’s accurate. Placeholder text also is not accessible.
* Display valid options as a user starts typing to confirm what they can choose.
* Add helper text that appears outside the field if someone makes an invalid entry.
  * Example: _Please enter a nine-digit phone number such as 555-555-5555._
* Include a button to explain what type of results users will get.
  * Example: **Search for your city**.

### Alerts
Alerts highlight important or time-sensitive information like deadlines.
 
### Info boxes
Put important information in an info box to help readers find it quickly while skimming. If the content is urgent, use an alert instead.
 
### Page indexes
An optional way to give users an outline of a long page is to add a page index at the top.

* Start with a brief sentence or two that states the most important takeaway on the page. Give this paragraph the "emphasized" class.
* Follow with the text  _On this page_: that introduces the index. Make it in Paragraph form with an "h3" class (not an H3 form, for accessibility reasons).
* Then add a bulleted, bolded list of the h2 headers on the page. Do not link subheaders. If something is important enough to appear in the page index, elevate it to an h2 header.
* Give the bulleted index list the class "toc" which will give it carat bullets and consistent styling.
* Make each h2 header an anchor link, and link each item in the index to its corresponding header.
