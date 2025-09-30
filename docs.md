---
title: docs
layout : page
excerpt: "Search for a page or post you're looking for"
subtitle: "Find articles, projects, and pages across the entire site."
---

<div class="sf-container">
  <header class="docs-header">
    <h1 class="sf-h1">Documentation Portal</h1>
    <p class="sf-text--large sf-text--muted">
      Welcome to our help center. Find articles, tutorials, and guides to get the most out of our product.
    </p>
  </header>
  <!-- Search Bar -->
  <div class="docs-search">
    <i class="ph-bold ph-magnifying-glass docs-search__icon"></i>
    <input type="search" id="docs-search-input" class="docs-search__input" placeholder="Search all articles...">
  </div>
  <!-- Category Grid -->
  <div class="docs-category-grid" id="docs-category-grid">
    {% assign docs_by_category = site.docs | group_by: "category" %}
    {% for category in docs_by_category %}
      {% assign items = category.items | sort: "order" %}
      <div class="docs-category-card" data-category-name="{{ category.name | downcase }}">
        <header class="docs-category-card__header">
          <i class="ph-bold ph-folder-simple"></i>
          <h2 class="docs-category-card__title">{{ category.name }}</h2>
          <span class="docs-category-card__count">{{ items | size }}</span>
        </header>
        <ul class="docs-category-card__list">
          {% for doc in items %}
            <li class="docs-category-card__item" data-doc-title="{{ doc.title | downcase }}">
              <a href="{{ doc.url | relative_url }}">
                <i class="ph-bold ph-file-text"></i>
                <span>{{ doc.title }}</span>
              </a>
            </li>
          {% endfor %}
        </ul> 
      </div>
    {% endfor %}
  </div>

</div>

<script>
    // assets/js/docs.js

document.addEventListener('DOMContentLoaded', () => {
  
  // ... your existing code for TOC and scroll-spying ...

  // --- Live Search for Docs Homepage ---
  const searchInput = document.getElementById('docs-search-input');
  const categoryGrid = document.getElementById('docs-category-grid');

  if (searchInput && categoryGrid) {
    const allCards = Array.from(categoryGrid.querySelectorAll('.docs-category-card'));
    const allItems = Array.from(categoryGrid.querySelectorAll('.docs-category-card__item'));

    searchInput.addEventListener('input', (e) => {
      const searchTerm = e.target.value.toLowerCase().trim();

      // If search is empty, show everything and exit
      if (searchTerm === '') {
        allCards.forEach(card => card.classList.remove('is-hidden'));
        allItems.forEach(item => item.classList.remove('is-hidden'));
        return;
      }
      
      // Filter individual doc items first
      allItems.forEach(item => {
        const title = item.dataset.docTitle || '';
        const isVisible = title.includes(searchTerm);
        item.classList.toggle('is-hidden', !isVisible);
      });

      // Then, hide any category cards that are now empty
      allCards.forEach(card => {
        const visibleItems = card.querySelectorAll('.docs-category-card__item:not(.is-hidden)');
        const hasVisibleItems = visibleItems.length > 0;
        card.classList.toggle('is-hidden', !hasVisibleItems);
      });
    });
  }
});
    </script>