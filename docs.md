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