---
title: Editing content
date: Last Modified 
permalink: /teams/content/editing.html
eleventyNavigation:
  key: Editing
  parent: Content
  order: 210
---

We edit content in [WordPress](https://live-covid19-ca-gov.pantheonsite.io/wp-login.php). It uses a what-you-see-is-what-you-get (WYSIWYG) editor that automatically applies formatting like bold and hyperlinks without the author needing to know how to code.

If something is not working the way you expect, your best bet is to select that block of text and choose the vertical ellipsis (three dots) to select **Edit as HTML**. This shows you the code view. Many times there's leftover code that's causing the problem.

## Right-side menu

When editing a WordPress post or page, there is a menu on the right side.

The _Post_ tab is selected by default. In this tab you can:

* Use the **Revisions** button to look at past versions of the page and undo changes
* Use the _URL Slug_ to create the page URL after the main URL (like https://covid19.ca.gov/page-I-made)
* Add tags

In the _Block_ tab, you'll mostly work in the **Advanced** section where you can:

* Create anchor links in _HTML anchor_.
  * Generally, only create anchor links to H2 header content.
  * Use lowercase letters and hyphens for spaces (the hyphens help screen readers read out the URL to those with low or no vision).
* Add [classes](https://teamdocs.covid19.ca.gov/teams/content/classes.html) in _Additional CSS class(es)_
  * Separate classes with spaces.
  * Two of the most commonly used classes are **wp-accordion** (the class for the title text of an accordion) and **wp-accordion-content** (the class for the body text). 
  * Only use _wp-accordion_ on headers. Follow the regular header rules to decide what level of header to use. No matter what header level is used, the _wp-accordion_ class will give the header a uniform visual appearance.
  * Remember to add _wp-accordion-content_ to every block inside the accordion. A block that does not have this class will appear outside the accordion.
  * You can add as many _wp-accordion-content_ blocks to the accordion as you like. They will be contained within the _wp-accordion_ block that precedes them.

## Tags

The main tags to know are:

* **staging-only** - This publishes the page only on the staging server. Use this to test how content appears or preview it for others.
  * Try to only stage content right before publication. It's easy to forget that content is staged and is not ready for publication. It also makes things complicated if the page needs other changes made but unapproved or unfinished staged content is in the way.
* **translate** - This tells our translation vendor to check the page for changes and push them to the translated versions of the page. This tag should be on every page unless otherwise specified.
* **fragment** - This marks a page or post as content that is used within another structure that’s been engineered behind the scenes. For example, the text of a homepage headline may be controlled by a short post tagged _fragment_ rather than a longer post that contains all the elements of the homepage. The structure will not work if the _fragment_ tag is not there.

Always check the tags before publishing. Sometimes tags drop off or do not load before publishing. It's especially important to check for _staging-only_ if changes are not ready to be published.

## Publishing

Use the **Update** button to publish changes. If you have made changes, but are not ready to publish to the live site, add the **staging-only** tag before you press _Update_. Do not use _Switch to draft_. This removes the page from the site.

After a post is submitted for publishing, you can track its progress in [GitHub Actions](https://github.com/cagov/covid19/actions). It usually takes a few minutes after the action completes before the change appears on the site. If you see in Actions that publishing for your page failed, ask a developer to take a look at what happened.

## Instant Preview

You can view any published content (with or without the **staging-only** tag) immediately after updating by using the [Preview Site](https://fa-go-wp-prev-02.azurewebsites.net/).  The most recent updates will appear at the top of the list.  Once you click on a preview link from the list, you can save the link for re-use or refresh your browser to reload the latest updates.

## Archiving pages

To archive a page:

1. Alert the engineering team that the page will be archived (you can do this up to two days in advance if you have lead time on the archiving). Create a GitHub issue for the engineers to perform the following tasks for the page to be archived:
  a. Remove translated page files
  b. Do a recrawl of quick answer questions (if needed)
2. Save the content (and any special code) in a Google Doc in case you need it later.
3. Remove the page from the [site menu](https://teamdocs.covid19.ca.gov/teams/content/menu.html).
4. Search WordPress for the page URL to see if it's linked to by any other page on the site. If so, remove or change the link.
  a. Search using only the slug (for example, /vaccines/) instead of the full URL (like https://covid19.ca.gov/vaccines). Many links do not use the full URL, just the slug.
5. Create a [redirect](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/teams/content/redirects.html) for the page (and any translated versions).
6. Confirm with the engineering team that they're ready for the page to be archived.
7. Find the page in the _Posts_ section of WordPress.
8. Hover your cursor over the row with the post. You'll see a set of options appear.
9. Select **Trash**. The post will move to the trash immediately without a confirmation screen.
10. Optional: Ask analytics to remove the page from the page feedback filters from the [Google Analytics Content Report](https://datastudio.google.com/u/0/reporting/4dc7f0ec-9b4c-403a-8d16-82909a204760/page/PyCVC).
11. Move the folder of draft Google Docs to the **Archived content** folder.

### Restoring posts or reusing URL slugs

It's easy to restore a post you recently removed by mistake.

1. Go to the _Posts_ section of WordPress.
2. At the top, underneath the word _Posts_, you'll see a list starting with _All_ and a number in parentheses. Select **Trash** at the end of the list.
3. Underneath the name of the archived page, select **Restore**.

If you want to reuse a URL slug from a page that was archived, check the [Page Redirect Table](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=1933&action=edit) in Wordpress to see if the slug is in the table.

* If it is, you can reuse it.
* If it is not in the table, the URL is going to a 410 page. This tells search engines that the page has been removed and there is no alternate content. Search engines now ignore the page. You will need to use a different URL.

To reuse a slug:

1. Create a new post in WordPress. The old post will not be available in Trash anymore unless it was deleted recently.
2. In the new post, go to **Settings** and select the **Post** tab.
3. Open the **Permalink** dropdown to update the URL slug to the one you are reusing. 

If you reuse a slug and had analytics remove it from the page feedback filters in the Google Analytics Content Report, you will need to ask them to add it back. Until the page is added to a filter, it will show up in the *Unassigned* filter.
