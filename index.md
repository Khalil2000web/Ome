---
layout: default
title: Ome Art Heal
author: "Ome"
published: true
---
<header>
<div class="container">
<h1>Ome Art Heal</h1>
<p>Capturing the world through my eyes.</p>
<a href="#gallery">GALLERY</a>
</div>
</header>
<section class="about">
<div class="container">
<h2>About</h2>
<p>A self-taught photographer with a heart for golden light, soft tones, and the beauty of everyday moments. Always chasing magic through my lens.</p>
</div>
</section>
<section id="gallery" class="gallery">
<div class="container">
<h2>Gallery</h2>
<div class="grid">
{% assign recent = site.data.gallery | sort: "date" | reverse | slice: 0, 6 %}
{% for item in recent %}
<img src="{{ item.url }}" alt="{{ item.title }}" loading="lazy" decoding="async" class="image">
{% endfor %}
</div>
</div>
</section>
<div class="cta-for-gallery"><a href="/gallery" rel="noopener noreferrer">view more</a></div>
