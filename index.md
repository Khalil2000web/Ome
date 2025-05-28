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
<a href="/gallery">GALLERY</a>
</div>
</header>
<section class="about">
<div class="container">
<h2>About</h2>
<p>A self-taught photographer with a heart for golden light, soft tones, and the beauty of everyday moments. Always chasing magic through my lens.</p>
</div>
</section>

<section class="home-page__gallery">
<h2>Preview</h2>
<div class="home-page__grid">
{% assign sorted = site.data.gallery | sort: "id" | reverse | slice: 0, 4 %}
{% assign recent = sorted | sort: "id" %}
{% for item in recent %}
<img src="{{ item.url }}" alt="{{ item.title }}" loading="lazy" decoding="async" class="image">
{% endfor %}
</div>
</section>

<div class="cta"><a href="/gallery">VIEW MORE</a></div>