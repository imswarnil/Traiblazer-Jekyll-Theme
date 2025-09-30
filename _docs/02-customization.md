
**`_docs/02-configuration.md`**
```yaml
---
title: Site Configuration
description: "Customize your site's title, author details, navigation, social links, and more via the _config.yml file."
order: 2
icon: gear
---

All major site-wide settings are controlled from the `_config.yml` file in the root of your project.

### Basic Settings

-   `title`: The main title of your site (e.g., "Your Name").
-   `description`: A short, site-wide description used for SEO meta tags.
-   `url`: The production URL of your site (e.g., "https://your-username.github.io").

### Navigation

The `navigation_header` section controls the links in your main navbar. You can add, remove, or reorder links easily:

```yaml
navigation_header:
  - title: Home
    url: /
  - title: Blog
    url: /blog/
  - title: Projects
    url: /projects/