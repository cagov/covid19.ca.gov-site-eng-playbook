---
title: Components
date: Last Modified 
permalink: /components/components.html
eleventyNavigation:
  key: Components
  parent: Components and styles
  order: 53
---

## Simple components and classes

These are components that can be applied by the content team without help from a developer.

### Page index

![Generic example of page index](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/page-index.jpg)

#### When we use it

We use the page index on every page with an introductory sentence to give people a sense of what’s on the page. The anchor links in the index allow people to get to the information they’re looking for, even if the page is long. Learn more about the page index in the [content style guide](https://teamdocs.covid19.ca.gov/components/when/content-style-guide.html#page-indexes).

#### How to apply

* Start with a brief sentence that states the most important takeaway on the page using the emphasized text class.
* Follow with _On this page_: in regular size.
* Make a bulleted, bolded list of the h2 headers on the page. Do not link subheaders. If something is important enough to appear in the page index, elevate it to an h2 header.
* Make each h2 header an anchor link and link each item in the index to its corresponding header.

#### Figma and Storybook documentation

### Highlight box

![Generic example of highlight box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box.jpg)

#### When we use it

Urgent information can be highlighted at the top of a page with a highlight box. It can include a right-aligned image next to body text and an action link (button), or can stand alone without these elements.

Use only one per page and position it at the top. Use it sparingly and get approval before publishing. Highlight boxes are an exception to our page style, not a rule--there should not be one on every page.

#### How to apply

For this highlight box with just text:

![Highlight box](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box.jpg)

The code is:

```
<div class="highlight">
<h2 class="h3 color-primary mt-0">Regional Stay Home Order ended January 25, 2021</h2>
<p>Counties returned to their appropriate tier under the Blueprint for a Safer Economy. Other state orders are still in place. See details on the <a href="https://covid19.ca.gov/stay-home-except-for-essential-needs/">About COVID-19 restrictions page</a>.</p>
</div><p></p>
```

For this highlight box with text and action link:

![Highlight box with action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-button.png)

The code is:

```
<div class="highlight">
<h2 class="h3 color-primary mt-0">Get information on safer school reopening</h3>
<p>If you’re a school leader, staff, or parent, the Safe Schools For All Hub is for you. Get updated information from the Department of Public Health, request technical assistance, or submit your concerns.
</p>
      <a class="button-lightblue font-size-1em" href="https://schools.covid19.ca.gov/">Visit the Safe Schools Hub</a>
</div><p></p>
```

For this highlight box with text, image, and action link:

![Highlight box with image and action link](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/highlight-box-with-image.jpg)

The code is:

```
<div class="highlight">
  <div class="row">
    <div class="col-md-9 order-last order-md-1">
      <h2 class="h3 color-primary mt-0">Sign up for COVID-19 vaccine notifications
      </h3>
      <p class="pr-0 pr-md-5">Get notified when it’s your turn to get the COVID-19 vaccine. If you're in Los Angeles or San Diego, you can also schedule your appointment.
      </p>
      <a class="button-lightblue font-size-1em" href="https://myturn.ca.gov/landing">Sign up now</a>
    </div>

    <div class="col-md-3 text-center py-4 p-0 pt-md-0 order-1 order-md-last">
      <a href="https://myturn.ca.gov/landing"><img class="img-fluid" loading="lazy" src="https://files.covid19.ca.gov/img/Vaccinate_ALL_58--en.png" alt="Map of California with text Vaccinate ALL 58 - Together we can end the pandemic." style="width:250px"></a>
    </div>
  </div>
</div>
```

#### Figma and Storybook documentation

### Accordion

#### When we use it

We use accordions in three situations:

* For content in question and answer format
* To group like content together
* To make pages simpler by initially hiding information that applies to less than 50% of our expected users

Do not use accordions just to make a page shorter. If everyone should see the content, it belongs in the main body of the page. Asking people to open an accordion to get info they need risks them missing it. They also have to take an action (clicking with their mouse or tapping their phone), which is extra effort.

Keep content in accordions short. If you have more than a few paragraphs to communicate, the content is better served being in the main body.

Content in accordions show up as *quick answers*, which means they can appear in search results on the site.

#### How to apply

To create an accordion, use the *wp-accordion* class to the text that will be the title of the accordion. Always make this content an H4 header.

To include a block inside the accordion, use the *wp-accordion-content* class. This must be applied to every block that you want inside the accordion. Missing a block will end the accordion and hide any blocks with the wp-accordion-content class below that missed block.

#### Chart drawer accordions

We often use a specialized accordion style to collapse some chart related details.

This may be created using custom HTML similar to the HTML described in the <a href="">design system's accordion component</a>. The differences for this version of an accordion on the covid site are the addition of the accordion-chart-drawer class and the use of a header tag inside the summary element.

Here is an example of the minimal code required:

```
<cagov-accordion class="accordion-chart-drawer">
  <details>
    <summary><h2>Chart information</h2></summary>
    <div class="accordion-body">
      accordion body content
    </div>
  </details>
</cagov-accordion></div>
```

Here is a real example with an additional width restriction applied above the link and chart drawer and the js-qa-exclude class added so this is not crawled as part of the site's quick answers:

```
<div class="row">
        <div class="col-lg-10 mx-auto">
<p class="small-text mt-3"><a href="https://data.chhs.ca.gov/dataset/vaccine-progress-dashboard">Overview of vaccine administration source data</a></p>

<div class="wp-block-cgb-block-chart-drawer js-qa-exclude">
<cagov-accordion class="accordion-chart-drawer">
  <details>
    <summary><h2>Chart information</h2></summary>
    <div class="accordion-body">
      <ul id="block-06834f88-b939-4857-ab6c-bc3709436cb8" class="small-text js-qa-exclude"><li>Data is not reported on weekends or state holidays. This data is processed on the first day following the weekend or holiday and updated here on the following day.</li><li>This chart includes vaccine doses administered and reported to state immunization registries. The vaccination rates are estimates based on best available information from vaccine records and Census data. These estimates may differ from those provided by local jurisdictions. Local estimates should be considered more accurate.</li><li>Rates are capped at 95%. This is consistent with CDC reporting practices. It prevents illogical values (like more than 100%) as a result of data entry issues.</li><li>Partially-vaccinated people are those receiving only one dose of the Pfizer or Moderna vaccine. Fully-vaccinated people are those who received two doses of the Pfizer or Moderna vaccines or the Johnson &amp; Johnson vaccine.</li><li>The statewide doses administered and delivered counts include all doses allocated to the California state jurisdiction as well as the CDC LTC Pharmacy and Retail Pharmacy Partnership Programs, Federal Dialysis Center Program, Federal Emergency Management Agency (FEMA) partner sites, and Health Resources and Services Administration (HRSA) partner sites. CDC Pharmacy Program doses are a subset of the doses delivered to California.</li><li>This data does not include doses delivered to the following federal agencies: Indian Health Service, Veterans Health Administration, Department of Defense, and Federal Bureau of Prisons.</li><li>Booster recipients includes anyone who is fully vaccinated and has received another dose of COVID-19 vaccine since August 13, 2021. This includes people who received booster doses and people who received additional doses.</li><li>This data will be consistently updated due to ongoing statewide vaccine record reconciliation efforts. Data may differ from those reported by local health jurisdictions and federal entities.</li><li>Where the county of residence was not reported, the county where vaccinated is used. This applies to less than 1% of vaccination records.</li><li>The sum of county-level vaccinations does not equal statewide total vaccinations because some out-of-state residents are vaccinated in California.</li></ul>
    </div>
  </details>
</cagov-accordion></div>
</div></div>
```

#### Figma and Storybook documentation

### Inline highlight box

#### When we use it

We use the inline highlight box to add a backgroung color to a section of content. This allows it to be highlighted without being put in the regular highlight box.

![Example of the blue highlight box in use](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/blue-highlight-example.jpg)

#### How to apply

To create an inline highlight box, use the *blue-highlight* class to the text.

![CSS class menu block with blue-highlight entered](https://cagov.github.io/covid19.ca.gov-site-eng-playbook//content/images/blue-highlight.jpg)
