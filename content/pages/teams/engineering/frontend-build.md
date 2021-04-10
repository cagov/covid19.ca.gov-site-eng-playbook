---
title: Front end build
date: Last Modified 
permalink: /teams/engineering/frontend-build/index.html
eleventyNavigation:
  key: Front end build
  parent: Engineering
  order: 102
---

Front end builds are run locally during development and before deployments inside git actions.

The front end build process includes:

* js packaging with rollup
* css purging controlled by gulp
* A separate es5 bundle created for pre-es6 browsers like IE11, which is delivered only to them via separate script tags using type=module and nomodule 
* Gulp watch, dev vs production
* [11ty static site generation](https://teamdocs.covid19.ca.gov/teams/engineering/eleventy/), which combines pages stubs with layouts and evaluates all includes generating the final HTML
* The .eleventy.js file controls additional transforms like localizing links to PDF files if a translated version is available
* The gulp process also controls some static file movement into final public directories and watch processes to retrigger during local development

The difference between running the local command **npm run dev** and the full build that runs in a git action with **npm run start** is that the es5.js bundle creation is skipped and all css and js inlining is bypassed. These differences speed up local runs of the build processes, allowing changes to css and js to take effect in a couple seconds without waiting for the full static site generation to run again.

The 11ty process takes much longer 15-30 seconds, depending on machine specs. This could be sped up massively by caching unchanged content. This feature is in development and should be available in an upcoming version of 11ty. There are already ways to take advantage of it now if you're using vue single file components on the server. This purely server-side component model seems like a promising alternative to our nunjucks templating. We currently mix templating using js template literals for some 11ty generated pages like the news section. The way 11ty allows you to easily mix templating languges allows for easy experimentation with different choices. As of February 2021, the bulk of the site layouts are using nunjucks.
