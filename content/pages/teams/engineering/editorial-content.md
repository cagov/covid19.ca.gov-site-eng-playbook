---
title: Content management in WordPress
date: Last Modified 
permalink: /teams/engineering/content-management/index.html
eleventyNavigation:
  key: Content management in WordPress
  parent: Engineering
  order: 103
---

We use WordPress to edit and mantain our content. WordPress powers 40% of the websites in the world. It has excellent editing features, numerous third party plugins. Its visual editing features have been iterated on for many years based on this large user base.

We do **not** use WordPress to deploy our content. More info on the <a href="/teams/engineering/publishing-pipeline/index.html">publishing pipeline is here</a>

<a href="https://as-go-covid19-d-001.azurewebsites.net/wp-admin/">Production WordPress instance</a>

## Different deployment environments

Use the ```staging-only``` tag to send an update to the <a href="https://staging.covid19.ca.gov">staging server</a> only. If this tag is not present the update will be published to both staging and production branches.

## Instant Preview

You can view any published content (with OR without the ```staging-only``` tag) immediately after updating by using the [Preview Site](https://fa-go-wp-prev-02.azurewebsites.net/).

Instant Preview uses the [11ty-serverless-preview-mode NPM package](https://github.com/cagov/11ty-serverless-preview-mode).
