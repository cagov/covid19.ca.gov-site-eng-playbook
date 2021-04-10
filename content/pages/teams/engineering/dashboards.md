---
title: Public dashboards
date: Last Modified 
permalink: /teams/engineering/dashboards/index.html
eleventyNavigation:
  key: Public dashboards
  parent: Engineering
  order: 116
---

Public-facing dashboards need to be held to more stringent performance and accessibility requirements in order to successfully serve an audience using a large variety of devices and connection strengths.

A dashboard that meets its design goals can fail to be useful if it does not:

* Render quickly in low-bandwidth, low-end device scenarios
* Present fully translated versions of data
* Allow navigation and interaction with assistive devices

An example that meets these goals is [California's commitment to health equity](https://covid19.ca.gov/equity/).

The choice of tech powering the charts had a big influence on our ability to meet these goals. A charting library helps you achieve these goals if it has:

* A small code footprint
* Integration hooks for translated strings
* Ability to customize the mouse free navigation experience

The code for the California's commitment to health equity page uses D3 to meet these goals successfully.

## Accessibility tutorial

Konstantin demonstrates how to make sure screenreader users can tab into chart elements and have the relevant tooltips read to them as they move around a data visualization using 3 lines of code

<iframe width="560" height="315" src="https://www.youtube.com/embed/id-RySRU7-E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
