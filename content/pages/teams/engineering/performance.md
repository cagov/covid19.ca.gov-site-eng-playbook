---
title: Accessible charts
date: Last Modified 
permalink: /teams/engineering/performance/index.html
eleventyNavigation:
  key: performance
  parent: Engineering
---

## Performance

Performance affects all users.

Fast render speed increases user satisfaction scores and slow sites decrease conversion levels: https://web.dev/why-speed-matters/

Slow-loading pages (taking 8.8 to 10.5 seconds to fully load) caused a 21% spike in blood pressure - https://au.pcmag.com/news/84535/study-finds-bad-web-design-is-killing-us-all-with-stress

### Performance is an equity issue

Low cost phones suffer disproportionately when encountering performance problems caused by large javascript code size

Here is a side by site comparison of the render speed of the same chart written in tableau and D3 measured using Moto G4 device setting on webpagetest
<iframe width="560" height="315" src="https://www.youtube.com/embed/xki_Jo0NlM4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


The amount of code being executed on the device is as important as delays delivering compressed files.
https://nolanlawson.com/2021/02/23/javascript-performance-beyond-bundle-size/

Asking less capable devices to execute MBs of javascript takes so long to become interactive the page is useless and inexpensive devices like amazon fire will often crash. We don't see these problems when we test our D3 dashboards on low end devices because they deliver interactive charts with much smaller code size.

## Translations

We are currently delivering deep translations all the way down to chart labels and mouseovers in our D3 charts

<img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/viet-chart.jpg">


Tableau charts on covid19.ca.gov are not translated at all

## Voiceover

Providing valid tabindex, keyboard focus events and appropriate labels can deliver an equivalent experience for users of assistive technologies

<iframe width="560" height="315" src="https://www.youtube.com/embed/gjkyxqUEpbk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Failing to take these steps will make important elements unusable

Here is an attempt to use voiceover on a tableau embed. The elements are keyboard navigable but there is no information the screenreader can use
<iframe width="560" height="315" src="https://www.youtube.com/embed/mI2jFD6Wbdo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Combining voiceover and translations

<iframe width="560" height="315" src="https://www.youtube.com/embed/zJGe0Xy8sqk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

