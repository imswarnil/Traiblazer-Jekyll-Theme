---
layout: home
title: ImSwarnil — Filmmaker • Software Engineer • Storyteller
hero_title: "Hi, I'm Swarnil — I ship beautiful, reliable Salesforce experiences."
hero_subtitle: "Software engineer by day, filmmaker by night. I design systems, craft stories, and make dashboards sing."
hero_company: "Imswarnil Studio"
hero_location: "Bengaluru, India"
hero_image: /assets/img/hero.jpg
hero_image_alt: "Swarnil smiling with a camera and laptop"
hero_primary_cta_text: "See Projects"
hero_primary_cta_link: "#work"
hero_secondary_cta_text: "Contact Me"
hero_secondary_cta_link: "#contact"

recent_work_title: "Recent Work"
recent_work_link_text: "View all →"
recent_work_link: "/projects/"
recent_work_limit: 6
---

<!-- This is all you need on your homepage to display the hero -->
{% include hero.html %}


{% comment %}
============================================================================
_includes/hero.html  — Definitive Personal Portfolio Edition
Depends on: components/_hero.scss, abstracts/tokens.scss, mixins.scss
============================================================================
{% endcomment %}

<section class="hero" id="home" aria-label="Intro / Hero">
  <div class="sf-container">
    <div class="hero-grid">
      <!-- Left: Text -->
      <div class="hero__text">
        <h1 class="sf-h1">
          {{ page.hero_title | default: "Build with Clarity. Ship with Style." }}
        </h1>
        <p class="sf-text--large sf-text-muted hero__subtitle">
          {{ page.hero_subtitle | default: "I make Salesforce apps, analytics dashboards, and cinematic devlogs with just enough chaos to keep it interesting." }}
        </p>
        <div class="hero__meta" aria-label="Quick facts">
          <span>
            <i class="ph-bold ph-buildings" aria-hidden="true"></i>
            Currently at <strong>{{ page.hero_company | default: "Your Company" }}</strong>
          </span>
          <span>
            <i class="ph-bold ph-map-pin" aria-hidden="true"></i>
            {{ page.hero_location | default: "Bengaluru, India" }}
          </span>
        </div>
        <div class="hero__actions">
          {% include button.html
            text=page.hero_primary_cta_text | default: "See Projects"
            link=page.hero_primary_cta_link | default: "#work"
            variant=page.hero_primary_cta_variant | default: "brand"
            size="lg"
            icon=page.hero_primary_cta_icon | default: "briefcase"
          %}
          {% include button.html
            text=page.hero_secondary_cta_text | default: "Contact Me"
            link=page.hero_secondary_cta_link | default: "#contact"
            variant=page.hero_secondary_cta_variant | default: "neutral"
            size="lg"
            icon=page.hero_secondary_cta_icon | default: "paper-plane-tilt"
          %}
        </div>
      </div>
      <!-- Right: Media -->
      <div class="hero__media">
        <div class="hero__image-wrapper">
          <img
            src="{{ page.hero_image | default: '/assets/img/hero.jpg' | relative_url }}"
            alt="{{ page.hero_image_alt | default: 'Portrait of ' | append: site.title }}"
            width="800" height="800" loading="eager" decoding="async"
          >
        </div>
        <!-- Floating tags (edit freely) -->
        <span class="hero__tag hero__tag--1">Apex</span>
        <span class="hero__tag hero__tag--2">CRM Analytics</span>
        <span class="hero__tag hero__tag--3">SAQL</span>
        <span class="hero__tag hero__tag--4">LWC</span>
      </div>
    </div>
  </div>
</section>

<section class="recent-work" id="work" aria-labelledby="recent-work-title">
  <div class="sf-container">
    <header class="recent-work__header">
      <h2 id="recent-work-title" class="recent-work__title">
        {{ page.recent_work_title | default: "Recent Work" }}
      </h2>
      <a class="recent-work__link" href="{{ page.recent_work_link | default: '/projects/' | relative_url }}">
        {{ page.recent_work_link_text | default: "View all →" }}
      </a>
    </header>
    {% assign work_items = page.recent_work | default: site.data.work %}
    <div class="work-grid">
      {% for item in work_items limit: page.recent_work_limit | default: 6 %}
        <article class="work-card">
          <a href="{{ item.url | relative_url }}" class="work-card__media" aria-label="{{ item.title }}">
            {% if item.image %}
              <img
                src="{{ item.image | relative_url }}"
                alt="{{ item.image_alt | default: item.title }}"
                loading="lazy" decoding="async" width="1200" height="750">
            {% else %}
              <!-- fallback skeleton if no image -->
              <div aria-hidden="true" style="height:100%;
                   background: linear-gradient(90deg,
                     color-mix(in srgb, var(--sf-ink) 4%, var(--sf-bg-2)) 25%,
                     color-mix(in srgb, var(--sf-ink) 8%, var(--sf-bg-2)) 37%,
                     color-mix(in srgb, var(--sf-ink) 4%, var(--sf-bg-2)) 63%
                   );
                   background-size: 400% 100%;
                   animation: skel-shimmer 1.4s ease-in-out infinite;">
              </div>
            {% endif %}
          </a>
          <div class="work-card__body">
            <h3 class="work-card__title">
              <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
            </h3>
            {% if item.summary %}
              <p class="sf-text-muted">{{ item.summary }}</p>
            {% endif %}
            {% if item.meta %}
              <div class="work-card__meta">
                {% for m in item.meta %}
                  <span class="work-card__meta-item">
                    {% if m.icon %}<i class="ph-bold ph-{{ m.icon }}" aria-hidden="true"></i>{% endif %}
                    <span>{{ m.text }}</span>
                  </span>
                {% endfor %}
              </div>
            {% endif %}
            {% if item.tags %}
              <div class="work-card__tags" aria-label="Tags">
                {% for t in item.tags %}
                  <span class="work-tag">{{ t }}</span>
                {% endfor %}
              </div>
            {% endif %}
          </div>
          {% if item.cta_text %}
            <div class="work-card__footer">
              {% include button.html text=item.cta_text link=item.url variant=item.cta_variant | default: "neutral" size="sm" icon=item.cta_icon %}
            </div>
          {% endif %}
        </article>
      {% endfor %}
    </div>

  </div>
</section>


<article class="skeleton-card">
  <div class="media-wrap">
    <div class="sf-skeleton__media" id="ph-media"></div>
    <img id="real-media" src="/assets/hero.jpg" alt="Preview" loading="lazy" style="display:none; width:100%; height:auto; border-radius: var(--sf-radius-lg); box-shadow: var(--sf-shadow-md);" />
  </div>
  <div class="sf-4"></div>
  <div class="sf-skeleton__title" id="ph-title" style="max-width: 60%"></div>
  <div class="sf-skeleton-stack" id="ph-lines">
    <div class="sf-skeleton__line"></div>
    <div class="sf-skeleton__line" style="max-width: 80%"></div>
    <div class="sf-skeleton__line" style="max-width: 70%"></div>
  </div>
</article>

<script>
  // minimal demo swap: replace skeletons when image completes
  const img = document.getElementById('real-media');
  const phMedia = document.getElementById('ph-media');
  const phTitle = document.getElementById('ph-title');
  const phLines = document.getElementById('ph-lines');
  img.addEventListener('load', () => {
    phMedia.style.display='none'; phTitle.style.display='none'; phLines.style.display='none';
    img.style.display='block';
  });
  // if cached
  if (img.complete) img.dispatchEvent(new Event('load'));
</script>


<!-- ======================================================= -->
<!-- All your other homepage sections (Timeline, Work, etc.) -->
<!-- can now follow here, each in their own <section> tag.  -->
<!-- ======================================================= -->

<section id="work" class="sf-container" style="padding: var(--sf-8) 0;">
  <div class="sf-page-header" style="margin-bottom:var(--sf-4);">
    <h2 class="sf-h2">Featured Work</h2>
  </div>
  <!-- Your work cards grid would go here -->
</section>

<!-- etc. -->