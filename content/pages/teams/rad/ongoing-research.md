---
title: Ongoing Feedback collection 
date: Last Modified 
permalink: /teams/rad/research/ongoing-research.html
eleventyNavigation:
  key: Ongoing research
  parent: Research
  order: 340
---

Our ongoing UX methods and activities to collect feedback from our visitors include:

* **Per page feedback** to gather feedback at a page level
* **NPI** to gather longitudinal data
* **Feedback survey** to gather comments about the overall website
* **User experience (UX) audit** to review user flows across pages

We reccomend a collaborative approach across different skill sets to execute each activity. 

This rubric identifies skills and roles recommended to use each tool.

![Rubric](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/rubric-ongoing-base.jpg)

## 🗒️ Per page feedback

We capture user feedback at a per page level to better understand what pages are useful; what on the page is meaningful, confusing, or distracting; and how we can make them relevant to user needs. We use a native form with daily comments hosted on [github](https://cagov.github.io/comment-reports/?code=Hv0cGBn1ysN97obrScf5awD1lZUs6JDyctdTmJgoAE6Py9bjy1foag==#filterA) and weekly synthesis and anlysis on [Google Sheets](https://docs.google.com/spreadsheets/d/1vFK8Xw41JThyJUa6M0Lv4qvAoJ-TQ4VK-TUc82FVFZA/edit#gid=1414096076), combined with responses collected through a related Ethnio survey.

Here's how we create the per page feedback reports:

| Steps	| Process | Tools | Improvements | Team |
|-	|-	|-	|-	|-	|
| Export feedback data and import into system | The data goes into Azure Cosmos DB (a cross region, managed database). We have a webpage with a few components in this  [repo](https://github.com/cagov/comment-reports) that hits the cosmos db api and pulls out the data with query params	| Simple graph views based on our APIs hosted on github pages | | Engineer	|
| Review data | Public facing: access data searchable by date, content captain and URL. Every captain reviews their pages and the Researcher reviews homepage. 	| [Per page feedback data site](https://cagov.github.io/comment-reports/?code=Hv0cGBn1ysN97obrScf5awD1lZUs6JDyctdTmJgoAE6Py9bjy1foag==#filterA)	| 	| Content captains and Researcher 	|
| Download data from Ethnio | Download data from surveys on a weekly basis | Ethnio + spreadsheet | With an enterprise subscription we could use the API and create an automatic download 	| Data analyst  |
| Import data to spreadsheet | We created a [template](https://docs.google.com/spreadsheets/d/1vFK8Xw41JThyJUa6M0Lv4qvAoJ-TQ4VK-TUc82FVFZA/edit#gid=1414096076) to visualize the data from Ethnio 	| Spreadsheet | 	| Analyst 	|
| Share report with team 	| Every week we share the dashboard and themes and findings from previous week	| Email + Slack |	| Researcher and data analyst	|

Here's what per page feedback looks like in production:

![Per page feedback](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/per-page.jpg)

### Link to documents

* [PRD](https://docs.google.com/document/d/13v2skLxkah2Jh_7HLytNqnwUlyHkOhe23v5gWNHol4w/edit#heading=h.49bsm1xjzv4h)
* [Document tracking iterations & improvements](https://docs.google.com/document/u/1/d/18GJtj2nrW_Hs9S7GuSGn15LaKUJaorjXYm7mc041mxE/edit)

## 🌡️ NPI Survey

We use the NPI survey to gather longitudinal data from visitors to covid19.ca.gov and ca.gov to discover how attitudes and behaviors change in response to changes in policy, local, and/or state economy and other factors. We present the link to the survey to every 50th visitor on the covid19.ca.gov homepage and every visitor to the ca.gov homepage. This survey is maintained through [SurveyMonkey](https://www.surveymonkey.com/).

Here's how we create and update the NPI survey:

| Steps | Process | Tools | Improvements | Team	|
|-	|-	|-	|-	|-	|
| Design survey	| The Insights team designed the first version early on in March. Most questions remain the same to gather longitudinal data. We work with the engineering team to make changes to the frequency it's shown to visitors.	| SurveyMonkey	| 	| Insights team and Researcher	|
| Meet weekly	| The Insights team and some external volunteers meet to discuss results and future iterations	| Google Meet or Zoom	| 	| Insights team, researcher, volunteers	|
| Dump data daily on spreadsheet	| Every weekday morning we download SurveyMonkey data from the NPI survey from the previous day from 12:00 am to 11:59 pm and then upload it to the NPI raw data sheet with a new date	| [NPI raw data sheet](https://docs.google.com/spreadsheets/d/1mVNx5z21wByufIULhd0HVaFVhODgSzxHvPPVyBdyAxU/edit?pli=1#gid=1397690428) | 	| Aanyone with access to SurveyMonkey	|
| Review open ended questions and gather quotes | Insights team reviews open-ended questions to gather quotes for the GO book (delivered weekly). Quotes are chosen to reflect constant and frequent themes, new themes we want to surface, and edge cases we want to shed light on. |  | Opportunity to follow up with interviews with participants who provided their email. We began collecting emails on November 1, 2020, but have not done much with them. | Insights team, researcher	|

![Example of our NPI](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/NPI.jpg)

---

## 🚧 Feedback survey (footer)

We have a survey link in the footer for visitors to give general website feedback, suggestions, and comments. This is also maintained through SurveyMonkey.

Here's how to update the survey:

| Steps | Process | Tools | Team |
|-	|-	|-	|-	|
| Design survey or edit questions	| We have edited the questions to avoid cannibalization of other sources of feedback | Google Docs and SurveyMonkey | Researcher |
| Dump data daily | Download the data from SurveyMonkey and upload it to the [Google Sheet](https://docs.google.com/spreadsheets/d/1W_rowHqsi1kIEEUkkbyjdoWcDhGuf4ctj44nER5aDxU/edit#gid=325946802). Read the feedback each morning. | Spreadsheet | Anyone with access to SurveyMonkey |
| Review comments daily	| Share meaningful comments with the team via Slack channel | Slack or standup | Anyone with access to SurveyMonkey	|

![Example of our Feedback link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/Footer.jpg)

---

## 🔏 User experience (UX) audit

We perform a UX audit to identify common pain points across key user flows and roadbloacks and success points when performing a task. We can then improve the overall flow instead of just focusing on a specific page.

A team of a designer, researcher, and data analyst define key user tasks. They map out the entire user flow to get a clear picture of all the different pages and actions users take to perform the previously selected tasks. We use Miro, Google Docs, Google Slides, Spreadsheet, and Quicktime in this process.

Here's how we create and implement an UX audit:

| Steps | Process	| Team 	|
|-	|-	|-	|
| Design study | Meet to design the studying | Researcher, designer and data analyst |
| Create scenarios | Based on Google Analytics, Governor's Office priorities, and other feedback sources, create scenarios | Researcher, designer, and data analyst 	|
| Assign scenarios| Each team member choses one or more scenarios to perform the audit | Researcher, designer, and data analyst |
| Execute audit	| Identify the parts of the website that answered the user’s question in the scenario.| Researcher, designer, and data analyst	|
| Visualize audit | Create a map that shows all of the ways that a user might get there (including search). Visualize the steps through a flow chart, mind map, or something similar. | Researcher, designer, and data analyst |
| Uncover pain points | For each step in the flow, identify potential pain points that make the process difficult (like confusing labeling)	| Researcher, designer, and data analyst |
| Find themes | Synthesize pain points to determine themes/trends | Researcher, designer, and data analyst |
| Define heuristics | Create heuristics to reuse in future audits | Researcher and designer	|
| Score scenarios | Score each flow with the heuristics/usability rubric	| Researcher and designer |
| Create list of quick wins and big improvements | For each theme, create a list with small wins and big improvements. Try to introduce small wins immediately. Include big improvements in the next major redesign. | Researcher and designer |

### Documentation for December 2020-January 2021 UX audit

- [Summary](https://docs.google.com/document/u/1/d/1fyfGQfloku5ovLj3Bq2tn6FQjYM8tw4lvDfe-Z0GbLY/edit#heading=h.6r8cy3o5529n)
- [Themes](https://docs.google.com/document/u/1/d/1hk4J3etzyUev2IX6-EGPuGtU01TsSTRlnagDqVLv-hA/edit#heading=h.f6hemeb02rmh) 
- [Full documentation](https://docs.google.com/document/d/1NnjkKBpD169wF-J_HvC6VwH5LYvddT4HZ5dKZT469iQ/edit#)

![UX Audit](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/audit.jpg)
