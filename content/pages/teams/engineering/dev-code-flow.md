---
title: Development code flow
date: Last Modified 
permalink: /teams/engineering/devcodeflow/index.html
eleventyNavigation:
  key: Development code flow
  parent: How our team works
  order: 122
---

We follow these procedures for code movement to production during development:

* New branches are created from the production branch.
* Branch names use the ticket/description pattern, like _CCG-1287/bug-event-tracking-prefixes_.
* Mention the ticket number in commits, pull requests (PRs) or manually add the PR link to the ticket
* Merging to staging branch is not controlled, so people can merge there at will without waiting for any approvals.
* Creating new full site environments based on any branch is fine anytime. Spin up a new Azure Static Web App and it will push the deploy git action to the specified branch. These environments support dynamic new instances on the first two open PRs against them but will error on the third simultaneously open PR.
* Merge to preproduction and run final tests before merging to production branch. [Preproduction is browseable.](http://lemon-pond-07547b71e.azurestaticapps.net/)
* Remove any code from preproduction that's no longer destined for release.
* Open a PR to merge any code to production or preproduction.
* Add all developers as reviewers to any PR using **covid19-ca-gov-engineering** so we can all keep track of what's going on, help, and learn from each other.
* Approvals are required before merging to either preproduction or production.
* Merging downstream from production to preproduction or from either of those to staging can be done any time without approvals.
* Automated end to end tests should run when PRs are opened, not run when code is merged. This helps vet code changes without slowing down content updates because editorial updates are direct merges to production branch, not PRs.
