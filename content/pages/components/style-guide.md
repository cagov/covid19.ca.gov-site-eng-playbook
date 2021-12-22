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

Covid19.ca.gov follows the [Office of Digital Innovation content design principles](https://docs.google.com/document/d/1orQyak_oQ2dSrDBYCRjauHTIQE51QGE_Cn4TssYrNX0/edit?usp=sharing). We also use the [Office of Digital Innovation word list](https://docs.google.com/document/d/1ALvcGokcsDYpjtTZ94HaOXyNKTDOx2AUPrtAJpZ7iyk/edit?usp=sharing).

## Content about emerging situations

We aim to give people a sense of calm, control, and purpose. We want to:

* Make people feel they have just enough information to act
* Give them the most widely-applicable and urgent info.
 
For specific info, link to state agency content.

To prioritize, get an authoritative state-level response up first. This fights misinformation by providing the truth directly and clearly. When that’s up, we focus on questions we imagine or know people are asking.

Ask these questions when writing content:
* Is the state the right authority on this?
* Does another agency (federal, state, or local) have more detailed or current data?
  * If so, link to them.
* Will information change over time?
  * If so, link to where it will be kept up-to-date.
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

* Front-load your headings with keywords that people use in search. Put popular keywords first.
* Use sentence case. Capitalize only the first word and proper nouns. It’s friendlier and helps readers recognize proper nouns.
* Make the name of your page an h1 header. (WordPress does this automatically.) Only use one h1 header per page.
* Use header levels in ascending numerical order. Do not skip steps. It’s OK to repeat header levels.
* Always have at least one line of text between headers.
* Do not use header tags for full sentences or non-header body text.

Check your heading structure in Google Docs. Select **View** and **Show Document Outline** to confirm they nest appropriately.

### Lead class text
Lead class text makes text larger. Use it to explain the service or topic at the top of the page, underneath the h1. Only use one paragraph of lead class text per page. Use: <p class="emphasized">the text you want</p> in WordPress to create lead class text.

### Page URLs
Use the title of the page to create your URL. This helps search engines find the page. (WordPress will do this automatically.)

Replace spaces in the title with hyphens so search engines can read them. Delete the conjunctions, prepositions, and articles as long as the URL still keeps the same meaning.
* A page titled _Hire a licensed contractor for home improvements_ would become _/hire-licensed-contractor-home-improvements_.
* Don’t make _Growing up with diabetes_ into _/growing-diabetes_. This has a different meaning.

Any time the site name is spelled out in content, make it a hyperlink to the homepage.

### Bold, italics, underlining
Use bold to emphasize important information or keywords. We do not use italics for emphasis because it is harder to read.

Do not underline content. Web browsers often underline links automatically. Underlining non-link content confuses readers.

### Links and buttons
Use a button to highlight something the user wants to do, or to allow them to submit a form. Links are embedded in text instead of standing alone.

* Link to webpages instead of PDFs as much as possible. Webpages are more accessible across devices, more easily searched, and easier to load on browsers.
  * If you must link to a document, make it a PDF. Word documents, Excel sheets, and PowerPoint presentations require software to view them that people may not have.
  * Links to PDFs automatically get an icon
  * Indicate if the link is going to a file by providing its extension (like DOC or PPT) so people can choose if they want to download it.
* Make the link title match the title of the destination page as much as possible. This helps people know they arrived in the right place.
* When creating a button, be short, descriptive, and distinctive.
* Limit the number of links within the text more readable. Links are interruptive and can make text harder to read. If you have several relevant links, put them in a bulleted list after your main text.
* Have links support comprehension, not disrupt it. Do not link until it's all right to send the user away (after you've conveyed your point).
* Open links in the [same tab and window](https://www.w3.org/TR/WCAG20-TECHS/G200.html). This is the expected behavior, and thus it’s better for accessibility. If users want to open their own tab or window, they know how to.
* When you end a sentence with a link, do not include the period in the hyperlink.
* Always create dial links for phone numbers. This allows users, especially mobile users, to dial the number with one click.
  * The WordPress format for the link is `tel:123‑456‑7890`, and the HTML is `<a href="tel:123‑456‑7890">123‑456‑7890</a>`.
  * Use non-breaking hyphens when creating these hyperlinks. These allow phone numbers in Arabic translations to work. The hyphens above are non-breaking. To be sure you're using a non-breaking hyphen, you can also use **&#8209;**.

### Notes and disclaimers
When info in tables or graphs needs an explanation, follow it with a note to provide clarity. Make the note smaller to signal to the reader that it is secondary info. In WordPress, use this code in the HTML view to create smaller text:

`<p class="small-text"> … </p>`

## Content types
Some content comes across better in non-paragraph form. Bullet points, alerts, and info boxes can also make pages easier to scan. 

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
* Provide a high-level summary of the task.
* Keep the description short, no more than a few paragraphs.
  * If it cannot be condensed, make a guide instead.
* Link to content that already exists on an agency website. Do not duplicate it. Prepare users with the information they need before they select the link.

An example of a numbered list is [Hire a licensed contractor for home improvements](https://www.alpha.ca.gov/hire-licensed-contractor-home-improvements/).

### Questions and answers
Use the question and answer format sparingly. We recommend putting the content in regular paragraphs instead. This makes it easier to find.

If you must create a question and answer section, just call it _Questions and answers_. Do not add any information like _Questions and answers about financial help_. If questions and answers cluster around certain topics, create subheaders to organize them.

To prevent a question and answer or other accordion from showing up in search results, add this class to the accordion title block (which will already have the class **wp-accordion**): **js-qa-exclude**

### Highlight boxes
Put information people should be alerted to at the top of the page in a highlight box to help readers find it first when they open a page.
 
### Page indexes
Give people an outline of a long page with a page index at the top.

* Start with a brief sentence or two that states the most important takeaway on the page. Give this paragraph the "emphasized" class.
* Follow with the text  _On this page_: that introduces the index. Use a paragraph block with an **h3** class (do not use an H3 header, for accessibility reasons).
* Then add a bulleted, bolded list of the h2 headers on the page. Do not include any subheaders in this list. If something is important enough to appear in the page index, elevate it to an H2 header.
* Give the bulleted list the class **toc**. This will give it caret bullets and consistent styling.
* Use anchor links with each H2 header. Link each item in the index to its corresponding header.
  * Put a separator block in front of each H2 and put the anchor link on the separator. This creates a visually pleasing buffer of space at the top of the page when someone selects the link from the index.
