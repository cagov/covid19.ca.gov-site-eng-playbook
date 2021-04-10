---
title: Translations
date: Last Modified 
permalink: /teams/engineering/translations/index.html
eleventyNavigation:
  key: Translations
  parent: Content management in WordPress
  order: 112
---


The covid19.ca.gov uses a human-powered translation service provided by AvantPage. This vendor translates all content into the 7 most-frequently spoken languages in California:

* Arabic
* Chinese simplified
* Chinese traditional
* Filipino
* Korean
* Spanish
* Vietnamese

The initial English language content is created in WordPress. When we want a post to be sent to the translation vendor we add the tag _translate_ to the post.

--- Carter would you please clarify what the trigger is for AvantPage now. Are they looking for changes in the git repo now or is the publishing service still pinging their API? --- 

## Translation publishing pipeline

The AvantPage system is setup to remember common phrases and passages so we should not be charged for the entire word count if we send the same document to them repeatedly with minor modifications.

AvantPage opens pull requests (PRs) against the covid19.ca.gov repository when they have a new set of translations for any content update.

The translation review service cronjob: https://github.com/cagov/Cron/tree/master/CovidTranslationPrApproval runs every 5 minutes and merges these PRs.

It's possible for a translation update to cause a problem that breaks the build. We have a continuous integration check that runs against all PRs to make sure the build still works. If this check fails, the PR will not be merged by the translation review scheduled task. The PR will remain open and will show in the github list of pull requests as having failed the build check. In this case we need to identify the cause and ask AvantPage to fix the problem if they caused it.

## Development

You can run the Azure Functions locally using the debugger because we have configured them in the .vscode/launch.json file.

Trying to debug the scheduled functions stops with the scheduling feature so the launch.json points at a separate file which executes the real code for those functions.

All of these functions point at production data sources and branch as configured, so even when you run them in the debugger you will be affecting live codebases. Create breakpoints to stop the process before new data is committed during debugging.
