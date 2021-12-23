---
title: Creating a redirect
date: Last Modified 
permalink: /teams/content/redirects.html
eleventyNavigation:
  key: Redirects
  parent: Custom content management
  order: 232
---

The content team can create redirects without help from a developer.

You can create a redirect that sends a URL slug to: 

* Another page of the site, including to a specific anchor
* The home page
* An external site
* The 410 page

A redirect that is set on a URL slug sends visitors to that slug to a new location. This includes anchor links added to that slug. You cannot create redirects for individual anchors of the URL slug.

You'll need the URL of the:

* Page you're replacing
* Page you're redirecting to

Before you make a redirect, check these things first:

* Does this page already have a redirect? Avoid adding a second one. If there are two entries for the same URL in the redirect table, this will break publishing for the entire site.
* Is the page in the site navigation menu? If so, update the WordPress post called **Menu Links** by either:
  * Changing the link to go to the new URL
  * Removing the row that contains the link to the page that’s being redirected
* Are there links to this URL on our site? Search engines prefer that we use as few redirects as possible. Update the URL of these hyperlinks or remove them prior to putting a redirect in place.

Once that’s done:

1. Open the WordPress post called [Page Redirect Table](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=1933&action=edit) WordPress post.
  a. This post uses the _table-data_ tag. 
  b. You cannot stage changes to this post.
2. Create a new row at the bottom of the table.
3. In the _original_url_ column, enter the slug for the page you want to redirect.
  a. Include forward slashes at the beginning and end of the slug (for example: _/safer-economy/_). The redirect will not work without them.
4. In the _replacement_url_ column, enter the URL or the slug for the page you want to redirect to.
  a. If there is a page that has replacement content, set the redirect to that page.
  b. Include forward slashes at the beginning and end of any slug you use here too.
  c. To redirect the URL slug to the home page, include only a forward slash (/) in the destination column. Be aware that doing this may negatively impact the site’s search engine score.
  d. If there is no replacement content, leave the destination column blank. This prevents the site from getting a Soft 404 penalty.
  e. Check the redirect table to see if the page you’re archiving is the destination of any redirects. Update those destinations as appropriate.
5. If the URL you're redirecting to _original_url_ is a page that gets translated, add a new row for each translated version.
  a. If you’re pointing to a page on our site that gets translated, make your _replacement_url_ go to the corresponding translated version of our site, including the homepage.
7. Search the list for any instances of the URL you’ve added to the _original_url_ column.
  a. This prevents double redirects, which search engines do not like.
8. **Update** the page to begin redirecting.
