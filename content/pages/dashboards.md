---
title: Public dashboards
date: Last Modified 
permalink: /dashboards/index.html
eleventyNavigation:
  key: dashboards
  order: 0
  title: Public dashboards
---

Public facing dashboards need to be held to more stringent performance and accessibility requirements in order to successfully serve an audience using a large variety of devices and connection strengths.

A dashboard which meets its design goals can fail to be useful if it doesn't:
- Render quickly in low bandwidth, low end device scenarios
- Present fully translated versions of data
- Allow navigation and interaction with assistive devices

An example which meets these goals is [California's commitment to health equity](https://covid19.ca.gov/equity/)

The choice of tech powering the charts had a big influence on our ability to meet these goals. A charting library helps you achieve these goals if it has:

- A small code footprint
- Integration hooks for translated strings
- Ability to customize the mouse free navigation experience

The code for the [California's commitment to health equity](https://covid19.ca.gov/equity/) page uses D3 to meet these goals successfully. There are several examples of public facing dashboards the state has shipped which fail to meet these standards. They are extremely slow to render, do not attempt to integrate translations and skip deep accessibility. These shortfalls can make the information unusable for visitors with a cheaper phone, anybody temporarily in a low bandwidth environment, speakers of english as a foreign language or people who depend on assistive technology.

## Building with D3

ObservablesHQ is a great tool for experimenting with charts. Here are some basic examples which you can edit or fork without creating your own development environment.

#### Bar chart with filled in background:

<a href="https://observablehq.com/@aaronhans/test-background-fill"><img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/bar-chart.jpg" /></a>

#### Using scales

<a href="https://observablehq.com/@d3/learn-d3-scales?collection=@d3/learn-d3"><img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/d3-scales.jpg" /></a>

#### Shapes

<a href="https://observablehq.com/@d3/learn-d3-shapes?collection=@d3/learn-d3"><img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/d3-shapes.jpg" /></a>

#### Colored county map with rollovers:

<a href="https://observablehq.com/@aaronhans/ca-county-tiers"><img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/map-viz.jpg" /></a>

#### Animating

<a href="https://observablehq.com/@d3/learn-d3-animation?collection=@d3/learn-d3"><img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/d3-anim.jpg" /></a>
