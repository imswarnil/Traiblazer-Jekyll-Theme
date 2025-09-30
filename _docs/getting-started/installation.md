---
title: Installation
order: 1.2
layout : docs
description: Two ways to get started with the theme: GitHub Pages or local development.
---

## Option 1: The Quick Way (GitHub Pages)

This is the easiest method to get your site live for free.

1.  **Fork the Repository:** Click the "Fork" button on the top-right of the [theme's GitHub repository](https://github.com/your-repo/sfdc-jekyll-theme). This creates a copy under your own GitHub account.
2.  **Rename the Repository:** In your new forked repository, go to `Settings` and rename it to `your-username.github.io`. This is a special name that tells GitHub Pages to build and host the site.
3.  **Enable GitHub Pages:** In the repository `Settings`, navigate to the "Pages" section. Under "Source", select the `main` (or `master`) branch and click "Save".
4.  **Edit `_config.yml`:** Update the `title`, `description`, `author`, and especially the `url` to match your new site's address (`https://your-username.github.io`).

Your site will be live in a few minutes!

## Option 2: The Developer Way (Local Installation)

This method is for those who want to customize the theme heavily on their local machine before deploying.

### Prerequisites
- [Ruby](https://www.ruby-lang.org/en/documentation/installation/) (check version with `ruby -v`)
- [Bundler](https://bundler.io/) (install with `gem install bundler`)

### Steps
1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-repo/sfdc-jekyll-theme.git
   cd sfdc-jekyll-theme