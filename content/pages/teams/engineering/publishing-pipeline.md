---
title: Publishing pipeline
date: Last Modified 
permalink: /teams/engineering/publishing-pipeline/index.html
eleventyNavigation:
  key: Publishing pipeline
  parent: Content management in WordPress
  order: 110
---

The WordPress update link for posts points at our function-as-a-service (FAAS). WordPress ping service gets disabled if you check discourage search engines from indexing this site.

## Publishing service FAAS

We run a FAAS on Azure functions that receives the pings from WordPress updates and writes the latest data into the covid19 site repository at [https://github.com/cagov/wordpress-integration-api](https://github.com/cagov/wordpress-integration-api).

There is a URL to [check to see publishing pipeline status](https://fa-cdt-covid19-d-001.azurewebsites.net/WordPressService). Selecting the button on this page will show you the in-memory history in the FAAS, including the record of pings and last update found.

This service looks at the WordPress API, gets the latest changed posts, compares the hash value of the post body with the value in our git repository, and updates or writes new content to github. 

Any post with a _translate_ tag on it gets sent to AvantPage via the endpoint they provided.

If you run the wordpress-integration-api locally it will ping production WordPress and write to master and staging. You can trigger a translate ping manually by setting [this flag](https://github.com/cagov/wordpress-integration-api/blob/dbc325d103d1184a7dcb98d3173afee00dbfd167/WordPressService/index.js#L26).

We [automatically create the same hash](https://github.com/cagov/wordpress-integration-api/blob/dbc325d103d1184a7dcb98d3173afee00dbfd167/WordPressService/index.js#L21) github uses to identify files.

## Debugging and running crons

We've disabled a bunch of crons in the file launch settings file. The launch settings file is used by the VSCode debugger to trigger a single service inside of a repository that contains multiple services. You can run it independently, point at a single file to execute, and add breakpoints.

## Debugging the WordPress publishing service

This service is alone in a repo so you can run it locally more easily than the grouped cron services. Locally you'll use a different github token from the one assigned to the wpserviceuser that the Azure function uses when running regularly in the cloud. We had a problem a couple times when we downgraded the permissioins of the _wpservice_ user to write from admin. This stops it from being allowed to merge directly to production without approvals. The _wpservice_ user should maintain github admin rights on the covid19 repo so it can publish continuously.
