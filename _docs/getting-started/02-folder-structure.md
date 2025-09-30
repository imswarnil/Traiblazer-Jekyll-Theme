---
title: "Folder Structure Overview"
description: "Understand the key files and folders in the theme, including where to add content, customize styles, and change layouts."
keywords: "jekyll folder structure, _posts, _layouts, _includes, _sass"
group: "Getting Started"
order: 2
icon: "folder-simple"
---

Understanding the project structure is key to customizing the theme effectively. Here is an overview of the most important files and directories.

 # All documentation articles live here.

├── _includes/ # Reusable HTML snippets (navbar, footer, etc.).
├── _layouts/ # The main HTML templates for pages and posts.
├── _posts/ # Your blog posts go here.
├── _sass/ # All SCSS files for styling the theme.
├── assets/ # Images, main CSS file, and other assets.
├── pages/ # Your static pages like 'About' or 'Contact'.
├── _config.yml # The main configuration file for your site.
└── Gemfile # Defines the Jekyll plugins and dependencies.


### Key Directories Explained

-   **`_posts`**: This is where you'll spend most of your time. Create new Markdown files here to write blog posts. The filename must follow the `YYYY-MM-DD-your-post-title.md` format.

-   **`pages`**: For standalone pages like an "About Me" or "Contact" page. These don't require a date in the filename.

-   **`_sass`**: The heart of the theme's design. You can modify colors, fonts, and spacing in `_sass/abstracts/_tokens.scss`, or change component styles in `_sass/components/`.

-   **`_layouts`**: These are the master templates. `default.html` is the base, while `post.html` and `page.html` define the structure for your content. You'll rarely need to edit these unless you're making major structural changes.

-   **`_includes`**: Small, reusable chunks of HTML. For example, `navbar.html` is included in `default.html` to render the navigation on every page.