---
title: Content Management in WordPress
date: Last Modified 
permalink: /teams/engineering/content-management/index.html
eleventyNavigation:
  key: Content management in WordPress
  parent: Engineering
  order: 113
---

### Overview ###
Content creators need to be free to update content on their own, and engineers need to be able to ensure adherence to performance and usability standards.  A Content Management System (CMS) is the solution to keeping all that balanced.  Most CMS solutions rely on an application server that reads content data from a database.  The content data is created by content creators through edit pages, then the content consumers use a portal to view the finished product.  The portal serves the content with the appropriate headers and style information.

For the Covid19 site, CMS tools are not ideal from an engineering standpoint, because the scale of all the web traffic going through a single server would create scalability problems.  We need the content to deliver fast, and allow for caching wherever applicable.  Static content through a Content Delivery Network (CDN) is the best solution for large audiences.

While a static site is the best for performance, it’s not ideal for content creators.  Maintaining headers, footers, styles, images, links, Javascript and everything else the public would expect in a good website will be impossible to maintain without automation.  We need something in between.

We use Wordpress to edit our content.  Wordpress is the most popular CMS tools in the world. It has excellent editing features, numerous 3rd part plugins, and plenty of support all over.  It’s visual editing features out-of-the-box are perfect for most users.  We do NOT use Wordpress to deploy our content.

We have a custom service for deploying content.  The architecture is Node.JS Function as a Service (FaaS) in Azure.  Content editors in Wordpress create Wordpress “Posts” with the content to be deployed.  Wordpress pings the custom service when content is changed.  The service downloads all the content from Wordpress through the Wordpress API.  The service compares the content to the deployed 11ty snippets in GitHub, and then updates pages that changed.  The 11ty build turns those snippets into a static website and then the Github/Azure pipeline deploys the static site to production.  The service also sends pings to the translation service when translation tagged content is changed, so they can include translated content in future updates.



- Where is all the content -
- Basic page flow -
- All tags in use -
- data tables -
- Different deployment environments
- Normal publishing flow
- Translations

