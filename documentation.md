---
layout: nested
title: Documentation
navbaritem: true
subfolders:
  - 'nesteddemo'
files:
  - 'landingpage'
  - 'nestedpage'
---

# How to Configure this Site?

For this template we have created three major features:

* Fully adaptable color scheme
* Nested pages
* Landing page

The nested and landing pages are explained in detail in their own chapter (see the end of this site). 
The fully adaptable color scheme, as well as arbitrary collections (used for nested pages) are defined in the config.yml file in the root of the site's directory.

In order to adapt the color scheme have a look at the configuration file depicted below:

```
---
# You can look up the color names at http://materializecss.com/color.html
colors:
    primary_dark: black
    primary_light: grey-darken-1
    primary: grey-darken-3
    accent: light-blue
    primary_text: grey-darken-4
    secondary_text: grey-darken-1
    inverse_text: white
    divider: grey-lighten-1
    secondaryBackground: grey-lighten-4

collections:
  landingpage:
    output: true
  documentation:
    output: true
---
```

## Color Scheme

The interesting part is the **colors** property. The colors can be taken from the [materialize color palette](http://materializecss.com/color.html). Nearly all of the possible combination tend to look good... somehow ;)
The primary colors are those that are used the majority of time on this site, e.g. for the Heroheader, text, links, headers, and stuff like that. The accent color is used rather sparse throughout the site, as the name implies it's merley for setting accents.
The text color is rather selfexplanatory. The inverse text color(usually whit if the text is black or vice versa) is used for example in the button text of the Heroheader.
Secondary background is used for code sections and the landing page news section as background color. The divider color is used for what its name implies: dividers.

We recommend to play aroud with these colors to create a site that looks good to you. Remember that you have to restart the Jekyll Server each time you change the colors, as the configuration file is only readat startup.

## Nested Pages and Additional Collections

Usually Jekyll has a flat folder structure and it is not really easy to create a hierarchical structure of webpages. The best Jekyll offers is a hierarchy of posts and categories.
We have created a template (nested) that allows you to structure content hierarchically with a little additional information in the front matter of your pages.
In order to create new nested pages you usually create a new [collection in Jekyll](https://jekyllrb.com/docs/collections/). For the use of **nested** templates have a look at the [Nested Page Documentation](/documentation/nestedpage.html)