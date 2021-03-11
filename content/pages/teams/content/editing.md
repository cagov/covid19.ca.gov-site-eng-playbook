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

## Tags

The two main tags to know about are:

* **staging-only** - This publishes the page only on the staging server. Use this to test how content appears or preview it for others.
  * Try to only stage content right before publication. It's easy to forget that content is staged and is not ready for publication. It also makes things complicated if the page needs other changes made but new content has been staged.
* **translate** - This tells our translation vendor to check the page for changes and push them to the translated versions of the page. This tag should be on every page unless otherwise specified.

Always check the tags before publishing. Sometimes tags drop off or do not load before publishing. It's especially important to check for _staging-only_ if changes are not ready to be published.

## Publishing

Use the **Update** button to publish. If you have made changes, but are not ready to publish to the live site, use the **staging-only** tag. Do not use _Switch to draft_. This unpublishes the page from the site.

After a post is submitted for publishing, you can track its progress in the [github Actions](https://github.com/cagov/covid19/actions). It usually takes a few minutes after the action completes before the change appears on the site. If you see in Actions that publishing for your page failed in, ask a developer to take a look at what happened.

## Archiving content

To archive a page:

1. Save the content (and any special code) in a Google Doc in case you need it later.
2. Create a [redirect](https://cagov.github.io/covid19.ca.gov-site-eng-playbook/teams/content/redirects.html) for the page (and any translated versions). (Remember to create redirects for any anchor links on the page too.)
3. Find the page in the _Posts_ section of WordPress.
4. Hover your cursor over the row with the post. You'll see a set of options appear.
5. Select **Trash**. The post will move to the trash immediately without a confirmation screen.

To restore a post:

1. Go to the _Posts_ section of WordPress.
2. At the top, underneath the word _Posts_, you'll see a list starting with _All_ and a number in parentheses. Select **Trash** at the end of the list.
3. Underneath the name of archived page, select **Restore**.
