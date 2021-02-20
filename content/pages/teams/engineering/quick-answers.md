---
title: Quick answers
date: Last Modified 
permalink: /teams/engineering/quick-answers/index.html
eleventyNavigation:
  key: Quick answers
  parent: Engineering
  order: 181
---

<img src="/content/images/quick-answers.png" />

## From the user’s perspective

Users are often searching with specific questions in mind. When we succeed in presenting a quick answer that directly answers their question it speeds up their search significantly. Refining our dataset is an ongoing process. We continually review the site searches, regularly adding to and updating the quick answer topics and content.

## How does it work technically

We wanted to combine off the shelf, managed cloud services so it would be cheap and run without maintenance. We didn’t want to take on the overhead of managing a bunch of cloud infrastructure, custom code or force our editorial team to duplicate content management work in another CMS.

We were able to achieve this in a way that any organization can duplicate. The cost to run this system is lwo because it falls under the cloud provider’s free tier even when our site gets a lot of traffic.

We use Azure cognitive search quick answers to provide all the backend features: the content database, the query evaluation logic and the endpoints for our frontend to call

We create the content by running <a href="https://github.com/cagov/Cron/tree/master/qnacrawler">a scraper</a> against our site regularly so the content is always updated based directly on our publicly published info. The only custom code is some logic to pull Q&A pairs from our frontend code. The scraper runs on Azure FAAS.

We feed user interaction data into our analytics tools so we can quickly see which quick answers were used most, which searches are being made, which don’t have any quick answers associated with them, and which answers were presented but ignored by our users. We use this data to refine our site content and the quick answers dataset gets updated by the site content changes.

We have reviewed some related solutions provided by:
- Open source work by governments like the Vermont Department of Health which was using some Azure tools to provide answers to people with a different UI: https://github.com/VermontDepartmentOfHealth/covid-bot 
- Other teams like our friends in <a href="https://covid19.ca.gov">New Jersey</a> who’ve implemented an interesting solution that we’ve been inspired by. They used a hosted Saas service to provide similar features. This didn't have an API available we could integrate when we were looking for this feature. Now it has comparable features to Azure cognitive search.