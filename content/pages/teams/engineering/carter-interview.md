---
title: Carter Medline on data pipelines
date: Last Modified 
permalink: /teams/engineering/data-pipeline-interview/index.html
---

Carter Medlin has setup data pipelines to support the <a href="https://covid19.ca.gov/equity/">covid19.ca.gov/equity/</a> and <a href="https://">covid19.ca.gov/state-dashboard/</a>". The charts on these dashboards get their data refreshed once daily. There is an agreement to publish at specific times in coordination with other state agencies. The data is moved into production separately from any of chart display code. The below excerpts highlight some of the techniques developed to cope with common issues like changing schedules, data quality, different approval workflows, working efficiently with git, error notifications in multiple channels.

## Data validation

Using schemas with data structure validation and thresholds checks are key to data pipelines running smoothly.

<iframe width="560" height="315" src="https://www.youtube.com/embed/t4Q7bDD-ACY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Working in the open

The Office of Digital Innovation chooses to work in the open. Our github repositories are under <a href="https://github.com/cagov">github.com/cagov</a>. This interview focuses on <a href="https://github.com/cagov/Cron">github.com/cagov/Cron</a>

<iframe width="560" height="315" src="https://www.youtube.com/embed/qFC-E7rJZQA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Data pull requests with manual approvals

Leveraging github for manual approval workflows provides permissions management and  a log of comments and approvals by default. It also  helps subject matter experts quickly view raw data differences and review updates in isolated staging environemtns. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/7qsFbpGK03A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Data pull requests with automated approvals

Using github tags to manage automated pull request approval processes helps provide flexibility to stop and restart workflows that will run automatically

<iframe width="560" height="315" src="https://www.youtube.com/embed/Qyf2fEzm1jY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Function triggers

How the covid19.ca.gov data pipeline code is scheduled and runs.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jbIdWLhp4y8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Writing to git

Combining multiple changes into scripted single commits with managed tree updates, working efficiently with the limits of the github API.

<iframe width="560" height="315" src="https://www.youtube.com/embed/sEU6tzi2UuE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Publishing with git actions

Using git actions to move approved data from git to production

<iframe width="560" height="315" src="https://www.youtube.com/embed/XFIDzfo8Hdk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Slack integration

Keeping the team informed via automated slack updates, error notifications

<iframe width="560" height="315" src="https://www.youtube.com/embed/NCCoAGBF7bA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>