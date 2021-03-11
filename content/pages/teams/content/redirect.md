---
title: Creating a redirect
date: Last Modified 
permalink: /teams/content/redirects.html
eleventyNavigation:
  key: Redirects
  parent: Custom content management
  order: 232
---

The content team can create redirects without help from a developer. You'll need the URL of the:

* Page you're replacing
* Page you're creating (which you'll set in WordPress using the _URL Slug_ field in the _Document_ tab of the right menu)

Before you make a redirect, check these things first:

* Is the page in the site navigation menu? If so, update the WordPress fragment titled **Menu Links** by either:
  * Changing the link to go to the new URL
  * Removing the row that contains the link to the page that’s being redirected
* Is anywhere on our site linking to this URL? Search engines prefer that as few redirects as possible as used. Update the URL of these hyperlinks or remove them prior to putting a redirect in place.
* Are there any anchor links on the page you need to account for?

Once that’s done:

1. Open the [Page Redirect Table](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=1933&action=edit) WordPress post.
2. Create a new row at the bottom of the table.
3. In the _original_url_ column, enter the slug for the page you want to redirect.
  a. Include forward slashes at the beginning and end of the slug (for example: _/safer-economy/_). The redirect will not work if the slashes are not included.
4. In the _replacement_url_ column, enter the URL or the slug for the page you want to send people to when they visit that URL.
  a. Include forward slashes at the beginning and end of any slug you use here too.
5. Leave the _Header label_ column blank.
6. If the URL you added to _original_url_ is a page that gets translated, add a new row for each translated version.
  a. If you’re pointing to a page on our site that gets translated, make your _replacement_url_ the corresponding translated version of our site.
7. Search the list for any instances of the URL you’ve added to the _original_url_ column.
  a. This prevents double redirects, which search engines do not like.
8. **Update** the page to begin redirecting.
