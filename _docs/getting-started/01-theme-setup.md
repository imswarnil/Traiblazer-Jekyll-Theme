---
title: "Theme Setup & Installation"
description: "A comprehensive guide to installing the SFDC Jekyll Theme, setting up dependencies, and getting your site ready for local development. Go from zero to running in 5 minutes."
keywords: "jekyll theme, install jekyll, jekyll setup, github pages theme, sfdc jekyll"
group: "Getting Started"
order: 1
icon: "rocket-launch"
---

Welcome! This is the essential first step to using this theme. This guide provides everything you need to get the theme installed on your local machine and prepare for development.

### Core Concepts

This theme is a modern Jekyll project. It uses **SCSS** for styling and is optimized for deployment on **GitHub Pages**. All major configuration happens in the `_config.yml` file, and content is written in Markdown.

---

### Prerequisites

Before you begin, ensure you have the following software installed on your computer.

-   **Ruby:** Jekyll is a Ruby gem. We recommend using a version manager like `rbenv` or `rvm` to install a recent version of Ruby (e.g., 3.0 or higher).
-   **Bundler:** A gem that manages Ruby project dependencies. Install it by running:
    ```bash
    gem install bundler
    ```

---

### Installation

There are two primary ways to install and use this theme. We highly recommend the first method for its simplicity and integration with GitHub.

#### Method A: Fork on GitHub (Recommended)

1.  **Fork the Repository:** Navigate to the theme's [GitHub repository](https://github.com/your-username/your-repo-name) and click the "Fork" button. This creates a complete copy of the project under your own GitHub account.

2.  **Rename Your Fork:** For GitHub Pages to serve your site from the root URL (e.g., `your-username.github.io`), you must rename your forked repository to `your-username.github.io`. Go to your new repository's **Settings** tab and change the name.

3.  **Clone Locally:** On your computer, clone your newly created repository:
    ```bash
    git clone https://github.com/your-username/your-username.github.io.git
    ```

#### Method B: Manual Download

1.  Go to the theme's GitHub repository.
2.  Click the green "Code" button and select "Download ZIP".
3.  Extract the ZIP file to a location on your computer.