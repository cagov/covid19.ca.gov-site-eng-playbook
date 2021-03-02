---
title: Ongoing Feedback collection 
date: Last Modified 
permalink: /teams/rad/research/ongoing-research.html
eleventyNavigation:
  key: Ongoing research
  parent: Research
  order: 340
---

Ongoing UX methods and activities undertaken to carry out the collection of feedback from our visitors.  


1. **Per page feedback**
2. **NPI**
3. **feedback survey**
4. **UX Audit**

We reccomend a collaborative approach across different skill sets to successfully execute each activity. 


## Rubric with needed skills for each tools
This rubric will help the researcher identify skills/roles needed to use each of the tools mention in this section.

![Rubric](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/rubric-ongoing-1.jpg)

---

## 🗒️ Per Page Feedback
- We use this feature to capture **user feedback at a per page level** in order to better understand what pages are useful, what within the page is meanigful, confusing, distracting and how we can improve them **to make them relevant to user needs**. 
- We use a **native form with daily comments hosted on github** and **google sheets with a weekly syntehsis and analysis** with responses collected from a link we host on ethn.io that is displayed after the visitor give a comment.
- **Links**: [sheets](https://docs.google.com/spreadsheets/d/1vFK8Xw41JThyJUa6M0Lv4qvAoJ-TQ4VK-TUc82FVFZA/edit#gid=1414096076) and [github](https://cagov.github.io/comment-reports/?code=Hv0cGBn1ysN97obrScf5awD1lZUs6JDyctdTmJgoAE6Py9bjy1foag==#filterA)
- These are the steps taken to use the per page feedback feature:


| Steps 	| Process 	| Tools 	| Improvements 	| Team 	|
|-	|-	|-	|-	|-	|
| Export feedback data and import in system 	| The data goes into Azure Cosmos DB (a cross region, managed database). We have a little webpage with a few web components on it in this  [repo](https://github.com/cagov/comment-reports)  that hits the cosmos db api and pulls out the data with query params	| Simple graph views based on our APIs hosted on github pages 	|  	| Engineer 	|
| Review data 	| Public facing: access data searchable by date, content captain and url<br>Every captain reviews their pages<br>Researcher reviews homepage  	| Access data here 	|  	| Content captains 	|
| Download data from ethnio links 	| Additional information is collected with an ethnio link: download data from surveys on a weekly basis 	| Ethnio + spreadsheet 	| If we had the enterprise subscription we could use the API and create an automatic download.  	| Data analyst  	|
| Import data to spreadsheet 	| We created a [template](https://docs.google.com/spreadsheets/d/1vFK8Xw41JThyJUa6M0Lv4qvAoJ-TQ4VK-TUc82FVFZA/edit#gid=1414096076) to visualize the data from ethnio  	| Spreadsheet 	|  	| Britt  	|
| Share template with team 	| Every week we share the dashboard + themes and findings from previous week  	| Email + slack 	|  	| Researcher and data analyst 	|


**Example of our feature**

![Per page feedback](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/per-page.jpg)

## Link to documents:
- [PRD](https://docs.google.com/document/d/13v2skLxkah2Jh_7HLytNqnwUlyHkOhe23v5gWNHol4w/edit#heading=h.49bsm1xjzv4h)
- [Document tracking iterations & improvements](https://docs.google.com/document/u/1/d/18GJtj2nrW_Hs9S7GuSGn15LaKUJaorjXYm7mc041mxE/edit)

---

## 🌡️ NPI Survey

- We have used the **NPI survey** to gather longitudinal data from visitors to covid19.ca.gov and ca.gov to **discover how attitudes and behaviors change as influenced by changes in policy, local and/or state economy** and other factors.
- We showcase the link to the survey to every 50th visitor on covid19.ca.gov (homepage) and static link in ca.gov (homepage)
- **Link**: https://www.surveymonkey.com/
- These are the steps taken to create and update the NPI survey:



| Steps 	| Process 	| Tools 	| Improvements 	| Team 	|
|-	|-	|-	|-	|-	|
| Design survey 	| The insights team designed the first version early on in March. Most questions remain the same to gather longitudinal data.  <br>Have to work with the eng team if we want to make changes to the frequency of delivery. Currently delivering to every 50th visitor on covid19.ca.gov and a static link on ca.gov site 	| Surveymonkey 	|  	| Insights team and <br>Researcher 	|
| Meet weekly 	| The insights team and some external volunteers meet on a weekly basis to discuss results and future iterations 	| Google meets 	|  	| Insights team, researcher , volunteers 	|
| Dump data daily on spreadsheet 	| Every weekday morning we download SurveyMonkey data from the NPI survey from the previous day from 12:00 am to 11:59 pm and then uploads it to the NPI raw data sheet with a new date 	| [NPI raw data sheet](https://docs.google.com/spreadsheets/d/1mVNx5z21wByufIULhd0HVaFVhODgSzxHvPPVyBdyAxU/edit?pli=1#gid=1397690428) 	|  	| Aanyone with access to surveymonkey 	|
| Review open ended questions to gather quotes 	| Insights team will review open ended questions to gather quotes for the GO book which is deliver weekly.  The criteria to choose quotes is a balance between constant and frequently mentioned themes, new themes we want to surface and edge cases that we should shed light on 	|  	| Opportunity to follow up with interviews with participants who opted to provide email. Since 11/1 we collect emails but haven’t done much with it. 	| Insights team, researcher 	|

![Example of our NPI](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/NPI.jpg)


---

## 🚧 Feedback Survey (Footer)

- We created a **survey link** to provide a place on the website for visitors to **give general website feedback, suggestions and comments**. 
- We added a link on the footer. We believe the location on the footer follows other websites best practices and it doesn't interfere with the user tasks. 
- **Link**:  SurveyMonkey
- These are the steps taken to make us of the NPI survey:

| Steps 	| Process 	| Tools 	| Team 	|
|-	|-	|-	|-	|
| Design survey and/or edit questions 	| Over time we have made some edits to the questions to complement other sources of feedback and avoid cannibalization 	| Google docs + surveymonkey 	| Researcher 	|
| Dump data daily 	|  Download the data from SurveyMonkey and upload it [here](https://docs.google.com/spreadsheets/d/1W_rowHqsi1kIEEUkkbyjdoWcDhGuf4ctj44nER5aDxU/edit#gid=325946802). Read through the feedback each morning 	| Spreadsheet 	| Anyone with access to surveymonkey 	|
| Review comments daily 	| Share meaningful comments with the team, mostly via slack channel 	| Slack or standup 	| Anyone reading the comments 	|


![Example of our Feedback link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/Footer.jpg)

---

## 🔏 UX Auditing


- We performed an **ux audit** to **identify common pain points across key user flows**. The audit's goal is to uncover pain points, roadbloacks and success points when performing a task. With this information we can then improve the overall flow, instead of just focusing on a specific page. 
- We recruited a team of a designer, researcher and analyst and assigned different tasks to each member. We mapped out the entire user flow to get a clear picture of all the different pages and actions users take to perform specific tasks. 
- **Tools**:  miro, google docs, google slides, spreadsheet, quicktime
- These are the steps taken to create and implement an UX Audit:



| Steps 	| Process 	| Tools 	|
|-	|-	|-	|
| Design study 	| A small team of one designer, one researcher and one data analyst met to design the study 	| Researcher, designer and data analyst 	|
| Create scenarios 	| Based on google analytics, GO office priorities and other feedback sources we created 10 scenarios 	| Data analyst 	|
| Assign scenarios 	| Each team member chose one or more scenarios to perform the audit 	| Researcher, designer and data analyst 	|
| Execute audit 	| Each team member identified the parts of the website that provided an answer to the user’s question in the scenario. 	| Researcher, designer and data analyst 	|
| Visualize audit 	| Each member created a map that showed all of the ways that a user might get there (including search). Each one chose to visualize the steps involved through a flow chart, mind map, or something similar. 	| Researcher, designer and data analyst  	|
| Uncover pain points 	| For each step in the flow, the team identified:<br>potential “pain points” that made the process difficult (e.g. confusing labeling) 	| Researcher, designer and data analyst  	|
| Find themes 	| As a group we synthesized pain points to determine themes/trends  	| Researcher, designer and data analyst  	|
| Define heuristics 	| Defined our own heuristics to reuse in future audits 	| Researcher and designer	|
| Score scenarios 	| Scored each flow with the usability rubric 	|  	|
| Create list of quick wins and big improvements 	| For each theme, we created a list with small wins and big improvements<br>Small Wins: try to introduce them immediately. <br>Big Improvements:  large-scale improvements/problems that we would like to tackle in our next major redesign. 	| Researcher and designer 	|

## Links to documents:

- [Summary](https://docs.google.com/document/u/1/d/1fyfGQfloku5ovLj3Bq2tn6FQjYM8tw4lvDfe-Z0GbLY/edit#heading=h.6r8cy3o5529n)
- [Themes](https://docs.google.com/document/u/1/d/1hk4J3etzyUev2IX6-EGPuGtU01TsSTRlnagDqVLv-hA/edit#heading=h.f6hemeb02rmh) 
- [Full documentation](https://docs.google.com/document/d/1NnjkKBpD169wF-J_HvC6VwH5LYvddT4HZ5dKZT469iQ/edit#)

![UX Audit](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/audit.jpg)


---

