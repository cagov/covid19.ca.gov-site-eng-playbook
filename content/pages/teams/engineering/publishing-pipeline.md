---
title: Publishing pipeline
date: Last Modified 
permalink: /teams/engineering/publishing-pipeline/index.html
eleventyNavigation:
  key: Publishing pipeline
  parent: Engineering
  order: 111.2
---


WordPress update link for posts points at our FAAS
WordPress ping service gets disabled if you check discourage search engines from indexing this site

## Publishing service FAAS

We run a Function As A Service on Azure functions which receives the pings from WordPress updates and writes the latest data into the covid19 site repository: [https://github.com/cagov/wordpress-integration-api](https://github.com/cagov/wordpress-integration-api)

There is a url to check to see publishing pipeline status: [https://fa-cdt-covid19-d-001.azurewebsites.net/WordPressService](https://fa-cdt-covid19-d-001.azurewebsites.net/WordPressService) Hitting the button on this page will show you the in menory history in the FAAS including the record of pings, last update found.

This service looks at the WordPress API, gets latest changed posts, compares the hash value of the post body with the value in our git repository and updates or writes new content to github. 

Any post with a translate tag on it gets sent to AvantPage via endpoint they provided.

If you run the wordpress-integration-api locally it will ping production WP and write to master + staging.

Trigger a translate ping manually by setting this flag: https://github.com/cagov/wordpress-integration-api/blob/dbc325d103d1184a7dcb98d3173afee00dbfd167/WordPressService/index.js#L26

Carter figured out how to automatically create the same hash github uses to identify files: https://github.com/cagov/wordpress-integration-api/blob/dbc325d103d1184a7dcb98d3173afee00dbfd167/WordPressService/index.js#L21


## Debugging and running crons

Carter has disabled a bunch of crons in the file launch settings file. The launch settings file is used by the VSCode debugger to trigger a single service inside of a repository that contains multiple. You can run it independently, point at a single file to execute and add breakpoints.

## Debugging the WordPress publishing service

This service is alone in a repo so you can run it locally more easily than the grouped Cron services. Locally you will be using a different github token from the one assigned to the wpserviceuser that the Azure function uses when running regularly in the cloud. We had a problem a couple times when we downgraded the permissioins of the wpservice user to write from admin which stops it from being allowed to merge directly to production without approvals. The wpservice user should maintain github admin rights on the covid19 repo to be able to publish continuously.
