---
layout: default
title: Documentation
description: Your one-stop guide to building a stunning personal website, portfolio, and blog. Become a Trailblazer on the web.
---

<div class="sf-container">
  <header class="docs-home-header">
    <h1 class="sf-h1">{{ page.title }}</h1>
    <p class="sf-text--large sf-text--muted">{{ page.description }}</p>
  </header>

  <div class="docs-home-search">
    <i class="ph-bold ph-magnifying-glass docs-home-search__icon"></i>
    <input type="search" id="docs-search-input" class="docs-home-search__input" placeholder="Search documentation...">
  </div>
  <div class="docs-home-grid" id="docs-home-grid">
    {% assign categories = site.docs | where_exp: "item", "item.path contains '_index.md'" | sort: "order" %}
    {% for category_page in categories %}
      {% assign article_count = site.docs | where: "category_slug", category_page.category_slug | where_exp: "item", "item.path != category_page.path" | size %}
      <a href="{{ category_page.url | relative_url }}" class="docs-home-card" data-category-title="{{ category_page.category_title | downcase }}">
        <div class="docs-home-card__header">
          <i class="ph-bold ph-{{ category_page.category_icon | default: 'folder' }} docs-home-card__icon"></i>
          <h2 class="docs-home-card__title">{{ category_page.category_title }}</h2>
        </div>
        <p class="docs-home-card__description">
          {{ category_page.content | strip_html | truncatewords: 20 }}
        </p>
        <div class="docs-home-card__footer">
          <i class="ph-bold ph-book-open"></i>
          <span>{{ article_count }} articles</span>
        </div>
      </a>
    {% endfor %}
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
        const title = card.dataset.categoryTitle || '';
        const isVisible = title.includes(searchTerm);
        card.classList.toggle('is-hidden', !isVisible);
      });
    });
  }
});
</script>