# Traillazer — A Jekyll Theme for Salesforce Professionals

Clean, fast, and battle‑ready for your Salesforce trail. Built with **Jekyll** and **SCSS**, deploys on **GitHub Pages**, ships as a **PWA**, and tuned for **SEO**.

![Traillazer cover](docs/cover.png)

![Build](https://img.shields.io/github/actions/workflow/status/yourname/traillazer/ci.yml?label=Build\&logo=github)
![Pages](https://img.shields.io/badge/Deployed%20on-GitHub%20Pages-24292e?logo=github)
![Lighthouse](https://img.shields.io/badge/Lighthouse-95%2B-0A7?logo=lighthouse)
![License](https://img.shields.io/badge/License-MIT-0A7)

---

## Features

* **Fast** – minimal JS, critical CSS, prefetch hints
* **Responsive** – mobile → ultrawide, fluid typography
* **SEO friendly** – `jekyll-seo-tag`, `jekyll-sitemap`, OG/Twitter cards
* **PWA** – offline cache, manifest, icons
* **Open Source** – MIT licensed
* **SCSS Theming** – design tokens, utilities, dark mode
* **Salesforce‑first blocks** – Certification grid, Project cards (CPQ, CRM Analytics, LWC, Apex, Flows), Talks timeline, Skills badges
* **Content types** – Posts, Projects, Speaking, Pages
* **Search (opt‑in)** – Lunr.js

---

## Screenshots (placeholders)

* `docs/screenshot-home.png`
* `docs/screenshot-blog.png`
* `docs/screenshot-project.png`

> Replace images in `/docs` with your own.

---

## Quick Start

### A) Use as remote theme (recommended)

```yaml
# _config.yml
url: "https://yourname.github.io"
title: "Your Name — Salesforce Professional"
description: "Admin | Developer | Architect — Projects, Articles, Trailhead"
remote_theme: yourname/traillazer
plugins:
  - jekyll-feed
  - jekyll-sitemap
  - jekyll-seo-tag
  - jekyll-include-cache
  - jekyll-remote-theme
```

`Gemfile` (GitHub Pages):

```ruby
gem "github-pages", group: :jekyll_plugins
gem "jekyll-remote-theme"
```

### B) Clone and run locally

```bash
git clone https://github.com/yourname/traillazer
cd traillazer
bundle install
bundle exec jekyll serve
```

Open: [http://localhost:4000](http://localhost:4000)

---

## Structure

```
.
├─ _config.yml
├─ _data/
│  ├─ certifications.yml
│  ├─ skills.yml
│  └─ socials.yml
├─ _posts/
├─ projects/
├─ speaking/
├─ pages/
│  ├─ about.md
│  └─ resume.md
├─ assets/
│  ├─ scss/
│  │  ├─ _tokens.scss
│  │  ├─ _utilities.scss
│  │  └─ traillazer.scss
│  ├─ js/
│  │  ├─ pwa.js
│  │  └─ search.js
│  └─ icons/
└─ manifest.webmanifest
```

---

## Configuration

### Identity

```yaml
author:
  name: "Your Name"
  role: "Salesforce Developer / Architect"
  email: "you@example.com"
  location: "Bengaluru, India"

social:
  linkedin: "your-handle"
  trailblazer: "your-trailblazer-id"
  github: "yourname"
  youtube: "yourchannel"
```

### Salesforce Sections

```yaml
salesforce:
  certifications: true
  projects:
    - title: "CPQ Quote Dashboard"
      tags: [CPQ, LWC, Analytics]
      repo: "https://github.com/yourname/cpq-quote-dashboard"
      demo: "https://yourname.github.io/cpq-quote-dashboard"
    - title: "CRM Analytics Starter"
      tags: [CRM Analytics, SAQL]
```

### Theme Tokens (SCSS)

```scss
/* assets/scss/_tokens.scss */
:root {
  --sf-blue: #009ed9;
  --ink-900: #111217;
  --ink-600: #373a40;
  --bg: #ffffff;
  --bg-dark: #0d0f13;
  --brand: var(--sf-blue);
  --radius: 14px;
  --shadow: 0 8px 30px rgba(0,0,0,.08);
}
```

---

## SEO & PWA

* `jekyll-seo-tag`, `jekyll-sitemap`, canonical URLs
* Open Graph/Twitter cards via front‑matter
* `jekyll-feed` for RSS
* `manifest.webmanifest` + `assets/js/pwa.js` (service worker)

---

## Development

```bash
bundle exec jekyll serve --livereload
# or
JEKYLL_ENV=production bundle exec jekyll build
```

---

## Roadmap

* [ ] Theme switcher (light/dark/auto)
* [ ] i18n (multi‑language)
* [ ] Algolia DocSearch
* [ ] Structured data (Course/Event schemas)
* [ ] Netlify/Cloudflare Pages adapters

---

## Contributing

PRs are welcome. Please run `bundle exec jekyll build` before submitting. For new components, include a usage snippet and minimal CSS.

---

## License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2025 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
