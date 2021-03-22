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

The code for the California's commitment to health equity page uses D3 to meet these goals successfully. There are several examples of public facing dashboards the state has shipped that fail to meet these standards. They are extremely slow to render, do not attempt to integrate translations, and skip deep accessibility. These shortfalls can make the information unusable for visitors with a cheaper phone, anybody temporarily in a low bandwidth environment, speakers of English as a foreign language, or people who depend on assistive technology.
