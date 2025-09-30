# Traillazer — A Jekyll Theme for Salesforce Professionals

> Clean, fast, and battle‑ready for your Salesforce trail.
> Built with **Jekyll + SCSS**, deploys on **GitHub Pages**, ships as a **PWA**, and tuned for **SEO**.

<p align="center">
  <img src="docs/cover.png" alt="Traillazer theme cover" width="960"/>
</p>

<p align="center">
  <a href="https://github.com/yourname/traillazer/actions"><img alt="Build" src="https://img.shields.io/github/actions/workflow/status/yourname/traillazer/ci.yml?label=Build&logo=github"></a>
  <a href="https://pages.github.com/"><img alt="Pages" src="https://img.shields.io/badge/Deployed%20on-GitHub%20Pages-24292e?logo=github"></a>
  <img alt="Lighthouse" src="https://img.shields.io/badge/Lighthouse-95%2B-0A7?logo=lighthouse"/>
  <img alt="License" src="https://img.shields.io/badge/License-MIT-0A7"/>
</p>

---

## ✨ Highlights

* ⚡ **Fast**: minimal JS, critical CSS, lazy‑loaded images, prefetch hints
* 📱 **Responsive**: mobile → ultrawide, fluid typography, container queries
* 🔎 **SEO‑friendly**: `jekyll-seo-tag`, clean permalinks, Open Graph/Twitter cards
* 🗺️ **Sitemap & RSS**: `jekyll-sitemap`, `jekyll-feed`
* 🧭 **Search (optional)**: Lunr.js client‑side search
* 📦 **PWA**: offline support via Workbox, manifest + icons included
* 🎨 **SCSS theming**: design tokens, dark mode, utility classes
* ☁️ **Salesforce‑first components**:

  * Certification grid
  * Project/Package cards (CPQ, CRM Analytics, LWC, Apex, Flows)
  * Speaking & Events timeline
  * Skills badges + proficiency bars
* 🧪 **Blog + Docs**: Markdown components, code highlighting (Prism/Shiki)
* 🧰 **GitHub Pages ready**: push → publish, no Docker needed
* 🔁 **Open source**: MIT, PR‑friendly

---

## 🖼️ Screens (placeholders)

| Home                              | Blog                              | Project                                 |
| --------------------------------- | --------------------------------- | --------------------------------------- |
| ![Home](docs/screenshot-home.png) | ![Blog](docs/screenshot-blog.png) | ![Project](docs/screenshot-project.png) |

> Replace images in `/docs` with your own.

---

## 🚀 Quick Start

### Option A — Remote theme (recommended)

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

`Gemfile` (for GitHub Pages):

```ruby
gem "github-pages", group: :jekyll_plugins
gem "jekyll-remote-theme"
```

### Option B — Clone (local dev)

```bash
git clone https://github.com/yourname/traillazer
cd traillazer
bundle install
bundle exec jekyll serve
```

Visit: [http://localhost:4000](http://localhost:4000)

---

## 🧱 Content Model

```
.
├─ _config.yml
├─ _data/
│  ├─ certifications.yml       # Name, issuer, url, year
│  ├─ skills.yml               # Category, items, level (0–100)
│  └─ socials.yml              # LinkedIn, X, Trailblazer, GitHub
├─ _posts/                     # Blog posts
├─ projects/                   # Collection: portfolio projects
│  └─ cpq-quote-dashboard.md
├─ speaking/                   # Talks / events timeline
├─ pages/
│  ├─ about.md
│  └─ resume.md
├─ assets/
│  ├─ scss/
│  │  ├─ _tokens.scss          # Color/typography/radius tokens
│  │  ├─ _utilities.scss       # Spacing, grid, helpers
│  │  └─ traillazer.scss       # Main bundle
│  ├─ js/
│  │  ├─ pwa.js
│  │  └─ search.js
│  └─ icons/                   # Manifest + PWA icons
└─ manifest.webmanifest
```

---

## ⚙️ Configure

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

### Salesforce sections

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

### Theme tokens (SCSS)

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

## 🔍 SEO & PWA

* **SEO**: `jekyll-seo-tag`, `jekyll-sitemap`, canonical URLs, robots.txt
* **OG/Twitter**: front‑matter (title, description, image)
* **Feed**: `jekyll-feed`
* **PWA**:

  * `manifest.webmanifest` (name, short_name, theme_color, icons)
  * `assets/js/pwa.js` (Service Worker w/ Workbox)
  * Offline cache for key routes (configurable)

---

## 🧩 Components (includes)

* `{% include certification-grid.html %}`
* `{% include project-card.html title="CPQ Dashboard" %}`
* `{% include badge.html text="LWC" tone="blue" %}`
* `{% include metric.html label="Dashboards" value="42" %}`

> All components are pure HTML/SCSS—no frameworks—so Lighthouse stays happy.

---

## 🧪 Development

```bash
bundle exec jekyll serve --livereload
# or
JEKYLL_ENV=production bundle exec jekyll build
```

**Performance tips**

* Use `.webp` images and set width/height.
* Keep hero under 120 KB.
* Critical CSS is inlined for above‑the‑fold.

---

## 🛣️ Roadmap

* [ ] Theme switcher (light/dark/auto)
* [ ] i18n multi‑language
* [ ] Algolia DocSearch option
* [ ] Structured data (Course/Event schemas)
* [ ] Netlify & Cloudflare Pages adapters

---

## 🤝 Contributing

PRs are welcome!

1. Fork → create branch → commit → open PR
2. Run `bundle exec jekyll build` before submitting
3. For new components, include a usage snippet and minimal CSS

---

## 🧾 License

**MIT License** — see [`LICENSE`](LICENSE).

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

---

## 📦 Starters & Demo (update me)

* Theme repo: `https://github.com/yourname/traillazer`
* Starter site: `https://github.com/yourname/traillazer-starter`
* Live demo: **coming soon**
* Lighthouse report: **coming soon**
