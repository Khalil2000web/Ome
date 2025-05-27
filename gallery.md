---
layout: default
title: Gallery
permalink: /gallery/
author: "Ome"
date: 2024-05-25 10:00:00
last_modified_at: 2025-05-25 10:30:00
published: true
---
<div id="imageModal" class="modal" tabindex="-1" role="dialog" aria-modal="true" ><button aria-label="Close modal" title="Close" type="button" class="close"><svg aria-hidden="true" focusable="false" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 16 16"><path stroke="white" strok-width="2" d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"/></svg></button><img class="modal-content" id="modalImg"></div>
<section class="gallery" style="padding-top:30px;">
<div class="container">
<h2>Gallery</h2>
<div class="grid">
{% assign sorted = site.data.gallery | sort: "id" %}
{% for item in sorted %}
<div class="image-wrapper" data-url="{{ item.url }}">
<img src="{{ item.url }}" alt="{{ item.title }}" loading="lazy" decoding="async" class="image">
</div>
{% endfor %}
</div>
</div>
</section>