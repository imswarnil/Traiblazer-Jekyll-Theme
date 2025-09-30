---
layout: default
title: Documentation
---

<div class="sf-container">
  <header class="docs-home-header">
    <h1 class="sf-h1">SFDC Theme Documentation</h1>
    <p class="sf-text--large sf-text--muted">
      Your one-stop guide to building a stunning personal website, portfolio, and blog. Become a Trailblazer on the web.
    </p>
  </header>

  <div class="docs-home-search">
    <i class="ph-bold ph-magnifying-glass docs-home-search__icon"></i>
    <input type="search" id="docs-search-input" class="docs-home-search__input" placeholder="Search documentation...">
  </div>

  <div class="docs-home-grid" id="docs-home-grid">
    <!-- Card 1: Getting Started -->
    <a href="/docs/getting-started/" class="docs-home-card" data-category-title="getting started">
      <div class="docs-home-card__header">
        <i class="ph-bold ph-rocket-launch docs-home-card__icon"></i>
        <h2 class="docs-home-card__title">Getting Started</h2>
      </div>
      <p class="docs-home-card__description">
        Learn how to install, configure, and deploy your site for the first time. The perfect starting point for all users.
      </p>
      <div class="docs-home-card__footer">
        <i class="ph-bold ph-book-open"></i>
        <span>2 articles</span>
      </div>
    </a>
    <!-- Card 2: Customization -->
    <a href="/docs/customization/" class="docs-home-card" data-category-title="customization">
      <div class="docs-home-card__header">
        <i class="ph-bold ph-paint-brush docs-home-card__icon"></i>
        <h2 class="docs-home-card__title">Customization</h2>
      </div>
      <p class="docs-home-card__description">
        Make the theme your own. Dive into theming, colors, fonts, and layout options to personalize every aspect.
      </p>
      <div class="docs-home-card__footer">
        <i class="ph-bold ph-book-open"></i>
        <span>1 article</span>
      </div>
    </a>
    <!-- Card 3: Content -->
    <a href="/docs/content/" class="docs-home-card" data-category-title="content">
      <div class="docs-home-card__header">
        <i class="ph-bold ph-pen-nib docs-home-card__icon"></i>
        <h2 class="docs-home-card__title">Content & Features</h2>
      </div>
      <p class="docs-home-card__description">
        Discover how to write blog posts, create project pages, and leverage the theme's powerful features.
      </p>
      <div class="docs-home-card__footer">
        <i class="ph-bold ph-book-open"></i>
        <span>0 articles</span>
      </div>
    </a>
    <!-- Card 4: Contributing -->
    <a href="/docs/contributing/" class="docs-home-card" data-category-title="contributing help">
      <div class="docs-home-card__header">
        <i class="ph-bold ph-git-pull-request docs-home-card__icon"></i>
        <h2 class="docs-home-card__title">Contributing</h2>
      </div>
      <p class="docs-home-card__description">
        Want to help improve the theme? Find out how you can contribute to the project, report bugs, and suggest features.
      </p>
      <div class="docs-home-card__footer">
        <i class="ph-bold ph-book-open"></i>
        <span>0 articles</span>
      </div>
    </a>
    <!-- Card 5: Help & Support -->
    <a href="/docs/help/" class="docs-home-card" data-category-title="help support">
      <div class="docs-home-card__header">
        <i class="ph-bold ph-question docs-home-card__icon"></i>
        <h2 class="docs-home-card__title">Help & Support</h2>
      </div>
      <p class="docs-home-card__description">
        Stuck on something? Check out our frequently asked questions or find out how to get in touch with us for support.
      </p>
      <div class="docs-home-card__footer">
        <i class="ph-bold ph-book-open"></i>
        <span>0 articles</span>
      </div>
    </a>
  </div>
</div>
<script>
document.addEventListener('DOMContentLoaded', () => {
  const searchInput = document.getElementById('docs-search-input');
  const grid = document.getElementById('docs-home-grid');
  if (searchInput && grid) {
    const allCards = Array.from(grid.querySelectorAll('.docs-home-card'));
    searchInput.addEventListener('input', (e) => {
      const searchTerm = e.target.value.toLowerCase().trim();
      allCards.forEach(card => {
        // Search the title from the data-attribute
        const title = card.dataset.categoryTitle || '';
        const isVisible = title.includes(searchTerm);
        card.classList.toggle('is-hidden', !isVisible);
      });
    });
  }
});
</script>