---
# --- SEO & Metadata ---
title: "Theme Setup & Local Development"
description: "A comprehensive guide to installing the SFDC Jekyll Theme, setting up dependencies, and running a local server for development. Get your site running in 5 minutes."
keywords: "jekyll theme, install jekyll, jekyll setup, local development, github pages theme, sfdc jekyll"
# --- Content & Sorting ---
group: "Getting Started"
order: 1
icon: "rocket-launch"
---

Welcome! This is the essential first step to using the SFDC Jekyll Theme. This guide provides everything you need to get the theme installed on your local machine, run a development server, and see your new site in action.

## Core Concepts

This theme is a modern Jekyll project. It uses **SCSS** for styling and is optimized for deployment on **GitHub Pages**. All major configuration happens in the `_config.yml` file, and content is written in Markdown.

---

## Part 1: Prerequisites

Before you begin, ensure you have the following software installed on your computer. These are standard for modern web development.

-   **Ruby:** Jekyll is a Ruby gem. We recommend using a version manager like `rbenv` or `rvm` to install a recent version of Ruby (e.g., 3.0 or higher).
-   **Bundler:** A gem that manages Ruby project dependencies. Install it by running:
    ```bash
    gem install bundler
    ```

---

## Part 2: Theme Installation

There are two primary ways to install and use this theme. We highly recommend the first method for its simplicity and integration with GitHub.

### Method A: Fork on GitHub (Recommended)

This is the fastest way to create your own site based on this theme.

1.  **Fork the Repository:** Navigate to the theme's [GitHub repository](https://github.com/your-username/your-repo-name) and click the "Fork" button in the top-right corner. This creates a complete copy of the project under your own GitHub account.

2.  **Rename Your Fork:** For GitHub Pages to serve your site from the root URL (e.g., `your-username.github.io`), you must rename your forked repository to `your-username.github.io`. Go to your new repository's **Settings** tab and change the name.

3.  **Clone Locally:** On your computer, clone your newly created repository:
    ```bash
    git clone https://github.com/your-username/your-username.github.io.git
    ```

### Method B: Manual Download

If you prefer to work locally without forking, you can download the theme directly.

1.  Go to the theme's GitHub repository.
2.  Click the green "Code" button and select "Download ZIP".
3.  Extract the ZIP file to a location on your computer.

---

## Part 3: Running the Local Development Server

Once you have the theme files on your local machine, you need to install the specific Jekyll plugins and gems it depends on.

1.  **Navigate to the Project Directory:**
    Open your terminal or command prompt and change into the theme's root folder.
    ```bash
    cd your-username.github.io
    ```

2.  **Install Dependencies:**
    Bundler will read the `Gemfile` in the project and install all the necessary gems.
    ```bash
    bundle install
    ```
    This command only needs to be run once, or after the `Gemfile` has been updated.

3.  **Start the Server:**
    This command builds your site and starts a local web server.
    ```bash
    bundle exec jekyll serve
    ```
    You will see output in your terminal indicating the server is running.

4.  **View Your Site:**
    Open your web browser and navigate to the address shown in the terminal, which is usually:
    **[http://127.0.0.1:4000/](http://127.0.0.1:4000/)**

The server will watch for changes to your content and configuration files and automatically rebuild the site. Simply refresh your browser to see your updates. To stop the server, press `CTRL + C` in your terminal.