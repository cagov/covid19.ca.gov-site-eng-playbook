---
title: Accessible charts
date: Last Modified 
permalink: /teams/engineering/performance/index.html
eleventyNavigation:
  key: performance
  parent: Engineering
---

<style>
#navigation {
  display: none !important;
}
#main {
  padding-left: 0 !important;
}
iframe {
  max-width: 100%;
}
.footer-nav {
  display: none !important;
}
</style>

## Performance

Fast render speed <a href="https://web.dev/why-speed-matters/">increases user satisfaction scores and slow sites decrease conversion levels</a> 

Slow-loading pages (taking 8.8 to 10.5 seconds to fully load) <a href="https://au.pcmag.com/news/84535/study-finds-bad-web-design-is-killing-us-all-with-stress">caused a 21% spike in blood pressure</a>

<iframe width="560" height="315" src="https://www.youtube.com/embed/xki_Jo0NlM4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
There is a big difference in how fast charts display when we use tableau vs D3

### Performance is an equity issue

Low cost phones suffer disproportionately when encountering performance problems caused by large javascript code size

The amount of code being executed on the device is <a href="https://nolanlawson.com/2021/02/23/javascript-performance-beyond-bundle-size/">as important as delays delivering compressed files</a>.

Asking less capable devices to execute MBs of javascript:
- Takes so long to become interactive the page is useless
- Inexpensive devices like amazon fire will often crash

We don't see these problems when we test our D3 dashboards on low end devices because they deliver interactive charts with much smaller code size.

## Translations

We are currently delivering deep translations all the way down to chart labels and mouseovers in our D3 charts

<img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/viet-chart.jpg">

Tableau embeds on covid19.ca.gov are not translated at all

## Voiceover

Here is an example of successful support for screenreaders in our D# chart

<iframe width="560" height="315" src="https://www.youtube.com/embed/gjkyxqUEpbk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Providing valid tabindex, keyboard focus events and appropriate labels can deliver an equivalent experience for users of assistive technologies. Failing to take these steps will make important elements unusable

We aren't making our tableau embeds accessible

<iframe width="560" height="315" src="https://www.youtube.com/embed/mI2jFD6Wbdo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Data visualizations can work for everybody

This is an example of a chart in production built with D3
- It renders quickly even on low cost devices and older browsers
- The labels inside the chart are fully translated
- It works with assistive tech like VoiceOver

<iframe width="560" height="315" src="https://www.youtube.com/embed/zJGe0Xy8sqk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

