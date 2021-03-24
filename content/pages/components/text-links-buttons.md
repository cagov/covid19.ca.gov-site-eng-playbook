---
title: Text, links and buttons
date: Last Modified 
permalink: /components/text-links-buttons.html
eleventyNavigation:
  key: Text, links and buttons
  parent: Components and styles
  order: 52
---

## Text Stlyes

### Headers

#### When we use them

Headers are used to organize information. They allow readers to scan content and find what they’re looking for. Properly cascading headers help screen readers identify the hierarchy of information.

We have five levels of header available:

* H1 - Montserrat bold 700, font-size 2.3rem, line height 1.2
* H2 - Montserrat bold 700, font-size 2rem,  line height 1.2
* H3 - Roboto bold 700, font-size 1.5rem (24px),  line height 1.2
* H4 - Roboto bold 700, font-size 1.4rem (22.4px),  line height 1.2
* H5 - Montserrat bold 700 uppercase, font-size 0.8rem (13.6px),  line height 1.2

More information about when we use headers is available in the [content style guide](https://teamdocs.covid19.ca.gov/components/when/content-style-guide.html).

#### How to apply

When creating a block of text in WordPress, select the *Heading* option. It will default to creating an H2. Once you’ve created the block, you can change the level of header by selecting the *H2* button in the menu above the block.

Do not use H1 headers when creating content. These are automatically created by WordPress using the title of the post. Each page can only have one H1.

### Emphasized text (P large)

P large - Roboto regular 400, color #000000, font-size  1.45rem,  line height 1.5

#### When we use it

Emphasized text is used whenever we want to make regular paragraph text larger than other text. The most common scenario is the first sentence of a page as part of introducing the page index.

#### How to apply

You can add the _emphasized_ CSS class in the right menu.

![Block section in WordPress with emphasized class code](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/emphasized-class-in-block.jpg)

### Normal text (P)

P - Roboto regular 300, color #00000, font-size 1.2rem,  line height 1.5, paragraph spacing 1.2rem

#### When we use it

This is the default text size for covid19.ca.gov. Use it whenever you’re creating body text or other general information.

#### How to apply

This text size is applied by default. You do not have to do anything to make your text show up in the normal size.

### P small

P small - Roboto regular 400, font-size 0.95rem,  line height 1.5, paragraph spacing 0.95rem

#### When we use it

Small text is used as explanatory text, usually underneath charts, tables, and other data presentations. It gives additional detail that the majority of people do not need, but still needs to be present for accuracy.

#### How to apply

Open the *Block* menu on the right side of the WordPress post. Select *Advanced* and enter _small-text_ in the _Additional CSS class(es)_ field to make the entire block small text.

You can also open the HTML view of the block you’d like to make small. Add the _small-text_ class to the paragraph code that starts the text.

```
<p class="small-text">The positivity rate in the matrix above excludes people in state and federal prisons, US Immigration and Customs Enforcement facilities, US Marshal detention facilities, and Department of State Hospitals facilities.</p>
```

### P extra small

P extra small - Roboto regular 400, color #000000, font-size 0.75rem,  line height 1.5, paragraph spacing 0.75rem

#### When we use it

Extra small text is reserved for data visualizations and charts.

## Link Styles

### Text link



#### When we use it

Use a text link to send people to other parts of the covid19.ca.gov website.

#### How to apply

Highlight the text you want to have become a text link. A menu will appear over the text block. Select the chain icon. Enter the destination URL. Select *Enter* to create the link.

### External link icon



#### When we use it

Use an external link icon to tell people a link will take them away from covid19.ca.gov. This includes any sites that use a domain that includes covid19.ca.gov, but is not maintained by our team. It’s OK to use this formatting multiple times if there are multiple external links in one paragraph.

If a link goes to a PDF hosted on an external site, do not apply the external link icon code. We only use one link icon per link. It’s more important to tell people they’re going to a PDF than it is to tell them that it’s not hosted on our site.

#### How to apply

For this external link icon:

![External link icon](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/external-link.png)

The code is:

```
<p>After reading, you can request to <a class="external" href="https://state-of-california-agency.forms.fm/great-plates-delivered-food-provider-interest-form">volunteer or provide meals</a>.</p>
```

### PDF link icon

#### When we use it

Use a PDF link icon to tell people a link will take them to a PDF. Use this formatting on any link to a PDF document, regardless of who owns it. It’s OK to use this formatting multiple times if there are multiple external links in one paragraph.

#### How to apply

The PDF link icon is applied automatically when you create a hyperlink that directs to a URL ending in _.pdf_.

If you need to manually apply the PDF link icon, use this code:

![PDF link icon](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/pdf-link-icon.png)

The code is:

```
<p>More details about receiving meals are available in the <a class="pdf" href="https://files.covid19.ca.gov/pdf/great-plates-delivered-participants-faqs.pdf">participant FAQ</a>.</p>
```

## Buttons and calls to action (CTA)

### Action button (action link)



#### When we use it

An action link is styled as a button so it stands out. It is used for a high-priority link near the top of the page. Only use one action link per page. Using a leading icon is preferred, but optional. Always put a space after the icon.

#### How to apply

For this action link:

![Action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/action-link.jpg)

The code is:

```
<a class="action-link" href="https://covid19.ca.gov/sign-up-for-county-alerts/"><span class="ca-gov-icon-warning-circle"></span><strong> Sign up for county alerts</strong></a>
```

### User interface (UI) button

There are many standard color combinations for this button and arrow links. See the [Examples](https://staging.covid19.ca.gov/sample) page for a preview, and check its [Wordpress file](https://as-go-covid19-d-001.azurewebsites.net/wp-admin/post.php?post=6854&action=edit) for the code for each.

#### When we use it

These button styles are used in forms and search fields. For example, the search field on the State Dashboard or Equity page.

#### How to apply

To create an action button, use this code:

```
<div class="col-md-3 py-4">
    <button class="button-lightblue bd-4px">button</button>
</div>
```

### Arrow link



#### When we use it

This code makes a special navigation link that responds to hover-overs with motion and a color change. Use this only once per page.

#### How to apply

For this arrow:

![Arrow button](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/arrow-button.jpg)

Use this code:

```
<div class="row py-5 text-center">
    <div class="col-md-3 bg-blue py-4">
        <a href="#" class="link-arrow-white">
            <div class="link-arrow-label">Arrow</div>
            <cagov-arrow></cagov-arrow>
        </a>
    </div>
</div>
```
