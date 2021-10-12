---
title: Editing content
date: Last Modified 
permalink: /teams/content/editing.html
eleventyNavigation:
  key: Editing
  parent: Content
  order: 210
---

Content is edited in [WordPress](https://as-go-covid19-d-001.azurewebsites.net/wp-login.php). It uses a what-you-see-is-what-you-get (WYSIWYG) editor that automatically applies formatting like bold and hyperlinks without needing to know how to code.

If something is not working the way you expect, your best bet is to select that block of text and choose the vertical ellipsis (three dots) to select **Edit as HTML**. This shows you the code view. Many times there's leftover code that's creating the problem.

## The right menu

On the right side of a WordPress post is a menu.

The _Document_ tab is selected by default. In this tab you can:

* Use the **Revisions** button to look at past versions of the page and undo changes
* Use the _URL Slug_ to create the page URL after https://covid19.ca.gov/
* Add tags

In the _Block_ tab, you'll mostly work in the **Advanced** section where you can:

* Create anchor links
  * Generally, only create anchor links to H2 header content.
  * Use lowercase letters and hyphens for spaces (the hyphens help screen readers).
* Add classes in _Additional CSS class(es)_
  * Separate classes with commas.
  * Two of the most commonly used classes are **wp-accordion** (the class for the title text of an accordion) and **wp-accordion-content**. Remember to add wp-accordion-content to every paragraph inside the accordion.
  * Only use _wp-accordion_ on headers. Follow the regular header rules to decide what level of header to use. No matter what header level is used, the _wp-accordion_ class will give the header a uniform visual appearance.

## Tags

The two main tags to know about are:

* **staging-only** - This publishes the page only on the staging server. Use this to test how content appears or preview it for others.
  * Try to only stage content right before publication. It's easy to forget that content is staged and is not ready for publication. It also makes things complicated if the page needs other changes made but new content has been staged.
* **translate** - This tells our translation vendor to check the page for changes and push them to the translated versions of the page. This tag should be on every page unless otherwise specified.

Always check the tags before publishing. Sometimes tags drop off or do not load before publishing. It's especially important to check for _staging-only_ if changes are not ready to be published.

## Publishing

Use the **Update** button to publish. If you have made changes, but are not ready to publish to the live site, use the **staging-only** tag. Do not use _Switch to draft_. This unpublishes the page from the site.

After a post is submitted for publishing, you can track its progress in the [github Actions](https://github.com/cagov/covid19/actions). It usually takes a few minutes after the action completes before the change appears on the site. If you see in Actions that publishing for your page failed in, ask a developer to take a look at what happened.

## Instant Preview

You can view any published content (with OR without the **staging-only** tag) immediately after updating by using the [Preview Site](https://fa-go-wp-prev-02.azurewebsites.net/).  The most recent updates will appear at the top of the list.  Once you click on a preview link from the list, you can save the link for re-use, or simply refresh the browser to reload the latest updates.

## Archiving content

To archive a page:

1. Alert the engineering team that the page will be archived (you can do this up to two days in advance if you have lead time on the archiving). Create a Jira ticket for the the engineers to perform the following tasks for the page to be archived:
  a. Remove translated page files
  b. Do a recrawl of quick answer questions (if needed)
2. Save the content (and any special code) in a Google Doc in case you need it later.
3. Remove the page from the [menu navigation](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=7484&action=edit).
4. Search WordPress for the page URL to see if it's linked to by any other page on the site. If so, remove or change the link.
  a. Search using only the slug (for example, /vaccines/) instead of the full URL (like https://covid19.ca.gov/vaccines). Many links do not use the full URL, just the slug.
5. Create a [redirect](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/teams/content/redirects.html) for the page (and any translated versions).
  a. If there is a page that has replacement content, set the redirect to that page.
  b. If there is no replacement content, leave the destination column blank. This prevents the site from getting a Soft 404 penalty.
  c. Check the redirect table to see if the page you're archiving is the destination of any redirects. Update those destinations as appropriate.
6. Confirm with the engineering team that they're ready for the page to be archived.
7. Find the page in the _Posts_ section of WordPress.
8. Hover your cursor over the row with the post. You'll see a set of options appear.
9. Select **Trash**. The post will move to the trash immediately without a confirmation screen.
10. Optional: Ask Britt/analytics to remove the page from the page feedback filters from the [Google Analytics Content Report](https://datastudio.google.com/u/0/reporting/4dc7f0ec-9b4c-403a-8d16-82909a204760/page/PyCVC).
11. Move the folder of draft Google Docs to the **Archived content** folder.

### Restoring posts or reusing URL slugs

Restoring a post mistakenly removed is easy.

1. Go to the _Posts_ section of WordPress.
2. At the top, underneath the word _Posts_, you'll see a list starting with _All_ and a number in parentheses. Select **Trash** at the end of the list.
3. Underneath the name of archived page, select **Restore**.

If you want to reuse a URL slug from a page that was archived, check the [Page Redirect Table](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=1933&action=edit) in Wordpress to see if the slug is in the table.

* If it is, you can reuse it.
* If it is not in the table, the URL is going to a 410 page. This tells search engines that the page has been removed and there is no alternate content. Search engines now ignore the page. You will need to use a different URL.

To reuse a slug:

1. Create a new post in WordPress. The old post will not be available in Trash anymore unless it was deleted recently.
2. In the new post, go to **Settings** and select the **Post** tab.
3. Open the **Permalink** dropdown to update the URL slug to the one you are reusing. 

If you reuse a slug and had Britt/analytics remove it from the page feedback filters in the Google Analytics Content Report, you will need to ask them to add it back. Until the page is added to a filter, it will show up in the *Unassigned* filter.
