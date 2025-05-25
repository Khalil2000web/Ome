---
layout: default
title: Gallery
permalink: /gallery/
author: "Ome"
date: 2024-05-25 10:00:00
last_modified_at: 2025-05-25 10:30:00
published: true
---
<section class="gallery" style="padding-top:30px;">
<div class="container">
<h2>Gallery</h2>
<div class="grid">
{% assign sorted = site.data.gallery | sort: "date" | reverse %}
{% for item in sorted %}
<img src="{{ item.url }}" alt="{{ item.title }}" loading="lazy" decoding="async" class="image">
{% endfor %}
</div>
</div>
</section>
