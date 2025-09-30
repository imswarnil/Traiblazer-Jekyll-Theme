---
title: "Running a Local Server"
description: "Learn how to install theme dependencies and run a local Jekyll server to preview your site and see changes live."
keywords: "jekyll serve, bundle install, local development, jekyll server"
group: "Getting Started"
order: 3
icon: "monitor-play"
---

Once you have the theme files on your local machine, you need to install its dependencies and start the local development server to preview your site.

### 1. Install Dependencies

This command reads the `Gemfile` in the project and installs all the necessary gems, including Jekyll and its plugins. You only need to run this once initially.

1.  Open your terminal or command prompt.
2.  Navigate to the theme's root folder.
    ```bash
    cd your-project-folder
    ```
3.  Run the Bundler installation command:
    ```bash
    bundle install
    ```

### 2. Start the Development Server

This command builds your site and starts a local web server that watches for changes and automatically rebuilds.

```bash
bundle exec jekyll serve