---
title: Ongoing Feedback collection 
date: Last Modified 
permalink: /teams/rad/research/ongoing-research.html
eleventyNavigation:
  key: Ongoing research
  parent: Research
  order: 340
---

Ongoing activities undertaken to carry out the collection of feedback from our visitors or intended audience.  

---

# 🗒️ Per Page Feedback
- 🥅 **Purpose**: capture user feedback at a per page level in order to better understand what pages are useful and how we can improve them. 
- 🔦 **Method**: native form with daily comments hosted on github and google sheets with weekly analysis collected from a link we host on ethnio plus Google analytics.
- 🧰 **Tools**: [sheets](https://docs.google.com/spreadsheets/d/1vFK8Xw41JThyJUa6M0Lv4qvAoJ-TQ4VK-TUc82FVFZA/edit#gid=1414096076) and [github](https://cagov.github.io/comment-reports/?code=Hv0cGBn1ysN97obrScf5awD1lZUs6JDyctdTmJgoAE6Py9bjy1foag==#filterA)
- 🧩 **Setup and steps**: 

| Steps 	| Process 	| Tools 	| Improvements 	| Team 	|
|-	|-	|-	|-	|-	|
| Export feedback data and import in system 	| The data goes into Azure Cosmos DB (a cross region, managed database). We have a little webpage with a few web components on it in this  [repo](https://github.com/cagov/comment-reports)  that hits the cosmos db api and pulls out the data with query params - (@Aaron) 	| Simple graph views based on our APIs hosted on github pages 	|  	| Aaron Hans (engineer) 	|
| Review data 	| Public facing: access data searchable by date, content captain and url<br>Every captain reviews their pages<br>Researcher reviews homepage  	| Access data here 	|  	| Content captains 	|
| Download data from ethnio links 	| Additional information is collected with an ethnio link: download data from surveys on a weekly basis 	| Ethnio + spreadsheet 	| If we had the enterprise subscription we could use the API and create an automatic download.  	| Data analyst (Britt Allen) 	|
| Import data to spreadsheet 	| We created a [template](https://docs.google.com/spreadsheets/d/1vFK8Xw41JThyJUa6M0Lv4qvAoJ-TQ4VK-TUc82FVFZA/edit#gid=1414096076) to visualize the data from ethnio  	| Spreadsheet 	|  	| Britt (data analyst) 	|
| Share template with team 	| Every week we share the dashboard + themes and findings from previous week  	| Email + slack 	|  	| Researcher and data analyst 	|


**Example of our feature**

![Per page feedback](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/per-page.jpg)

## Link to documents:
- [PRD](https://docs.google.com/document/d/13v2skLxkah2Jh_7HLytNqnwUlyHkOhe23v5gWNHol4w/edit#heading=h.49bsm1xjzv4h)
- [Document with iterations](https://docs.google.com/document/u/1/d/18GJtj2nrW_Hs9S7GuSGn15LaKUJaorjXYm7mc041mxE/edit)

---

# 🌡️ NPI Survey

- 🥅 **Purpose**: gather longitudinal data from visitors to covid19.ca.gov and ca.gov to discover how attitudes and behaviors change as influenced by changes in policy, local and/or state economy, etc
- 🔦 **Approach**: link display to every 50th visitor on covid19.ca.gov (homepage) and static link in ca.gov (homepage)
- 🧰 **Tools**:  surveymonkey
- 🧩 **Setup and steps**: 


| Steps 	| Process 	| Tools 	| Improvements 	| Team 	|
|-	|-	|-	|-	|-	|
| Design survey 	| The insights team designed the first version early on in March. Most questions remain the same to gather longitudinal data.  <br>Have to work with the eng team if we want to make changes to the way and frequency of delivery. Currently delivering to every 50th visitor on covid19.ca.gov and a static link on ca.gov site 	| Google docs Surveymonkey 	|  	| Insights team (JP, Jeffrey)<br>Researcher 	|
| Meet weekly 	| The insights team and some external volunteers meet on a weekly basis to discuss results and future iterations 	| Google meets 	|  	| Insights team, researcher , volunteers 	|
| Dump data daily on spreadsheet 	| Every weekday morning, Karim (content designer) downloads SurveyMonkey data from the NPI survey from the previous day from 12:00 am to 11:59 pm and then uploads it to the NPI raw data sheet with a new date 	| NPI raw data sheet 	|  	| Karim (anyone with access to surveymonkey) 	|
| Review of open ended questions to gather quotes 	| JP from Insights team will review open ended questions to gather quotes for the GO book.  Criteria to choose quotes: it’s really balancing themes that are constant, frequently mentioned, new ones that feel like we want to surface them, as well as edge cases that feel like we should shed light on 	|  	| Opportunity to follow up with interviews with participants who opted to provide email. Since 11/1 we collect emails but haven’t done much with it. 	| Insights team, content designer 	|

![Example of our NPI](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/NPI.jpg)


---

# 🚧 Feedback Survey (Footer)

- 🥅 **Purpose**: provide a place on the website for visitors to give general website feedback, suggestions and comments
- 🔦 **Approach**: link on footer
- 🧰 **Tools**:  SurveyMonkey
- 🧩 **Setup and steps**:

| Steps 	| Process 	| Tools 	| Team 	|
|-	|-	|-	|-	|
| Design survey and/or edit questions 	| Over time we have made some edits to the questions to support and complement other sources of feedback  	| Google docs + surveymonkey 	| Researcher 	|
| Dump data daily 	| Karim downloads the data from SurveyMonkey and uploads it here. Karim reads through the feedback each morning 	| Spreadsheet 	| Karim (anyone with access to surveymonkey) 	|
| Review of comments daily 	| Share meaningful comments with the team, mostly via slack channel 	| Slack or standup 	| Karim or anyone reading the comments and feedback 	|


![Example of our Feedback link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/Footer.jpg)


---

# 🔏 UX Auditing


- 🥅 **Purpose**:  identify common pain points across key user flows 
- 🔦 **Method**: UX Audit where the internal team mapped out the entire user flow to get a clear picture of all the different pages and actions users take to perform specific tasks
- 🧰 **Tools**:  miro, google docs, google slides, spreadsheet, quicktime
- 🧩 **Setup and steps**: 


| Steps 	| Process 	| Tools 	|
|-	|-	|-	|
| Design study 	| A small team of one designer, one researcher and one data analyst met to design the study 	| Clara Gonzalez Sueyro (Researcher) and Adam Little ( designer) and Britt Allen (data analyst) 	|
| Create scenarios 	| Based on google analytics, GO office priorities and other feedback sources we created 10 scenarios 	| Britt Allen(Data analyst) 	|
| Assign scenarios 	| Each team member chose one or more scenarios to perform the audit 	| Britt, Clara, Adam and Jessica Lopez 	|
| Execute audit 	| Each team member identified the parts of the website that provided an answer to the user’s question in the scenario. 	| Britt, Clara, Adam and Jessica Lopez 	|
| Visualize audit 	| Each member created a map that showed all of the ways that a user might get there (including search). Each one chose to visualize the steps involved through a flow chart, mind map, or something similar. 	| Britt, Clara, Adam and Jessica Lopez 	|
| Uncover pain points 	| For each step in the flow, the team identified:<br>potential “pain points” that made the process difficult (e.g. confusing labeling) 	| Britt, Clara, Adam and Jessica Lopez 	|
| Find themes 	| As a group we synthesized pain points to determine themes/trends  	| Britt, Clara, Adam and Jessica Lopez 	|
| Define heuristics 	| Defined our own heuristics to reuse in future audits 	| Clara and Adam 	|
| Score scenarios 	| Scored each flow with the usability rubric 	|  	|
| Create list of quick wins and big improvements 	| For each theme, we created a list with small wins and big improvements<br>Small Wins: try to introduce them immediately. <br>Big Improvements:  large-scale improvements/problems that we would like to tackle in our next major redesign. 	| Clara and Adam 	|

## Links to documents:

- [Summary](https://docs.google.com/document/u/1/d/1fyfGQfloku5ovLj3Bq2tn6FQjYM8tw4lvDfe-Z0GbLY/edit#heading=h.6r8cy3o5529n)
- [Themes](https://docs.google.com/document/u/1/d/1hk4J3etzyUev2IX6-EGPuGtU01TsSTRlnagDqVLv-hA/edit#heading=h.f6hemeb02rmh) & [Metrics](https://docs.google.com/document/u/1/d/1hk4J3etzyUev2IX6-EGPuGtU01TsSTRlnagDqVLv-hA/edit#heading=h.f6hemeb02rmh)
- [Full documentation](https://docs.google.com/document/d/1NnjkKBpD169wF-J_HvC6VwH5LYvddT4HZ5dKZT469iQ/edit#)


![Theme recognition ](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/audit.jpg)

---
## Rubric with needed skills for each activity

![Rubric](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/content/images/rubric.jpg)

---

