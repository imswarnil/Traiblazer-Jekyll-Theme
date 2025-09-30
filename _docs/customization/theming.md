---
title: Theming & Colors
layout : docs
order: 2.1
description: How to change the look and feel of your site.
---

## Changing the Theme

The SFDC Jekyll Theme comes with multiple built-in themes. To change the theme for your entire site, simply update the `theme` variable in your `_config.yml` file.

You can also allow users to switch themes on the fly using the theme switcher in the navigation bar.

## Customizing Colors

All colors are controlled via CSS Custom Properties in the `_sass/abstracts/_tokens.scss` file. To change the primary brand color, simply update the `--sfdc-brand` variable:

```css
:root {
  --sfdc-brand: #ff0000; /* Change from blue to red */
}