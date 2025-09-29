---
layout: home
title: ImSwarnil — Filmmaker • Software Engineer • Storyteller

# --- Front Matter for the Hero Component ---
hero_title: "Creative chaos, engineered."
hero_subtitle: "I build <strong>Salesforce CRM Analytics</strong> solutions by day and craft cinematic stories by night. I bring a unique blend of technical precision and creative vision to every project."
hero_company: "Twilio"
hero_location: "Bengaluru, India"
hero_image: "/assets/Traiblazer-Profile.png" # IMPORTANT: Add your profile picture here
hero_image_alt: "A professional headshot of Swarnil Singhai"
---

<!-- This is all you need on your homepage to display the hero -->
{% include hero.html %}

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