---
layout: default
title: Gallery
permalink: /gallery/
author: "Ome"
date: 2024-05-25 10:00:00
last_modified_at: 2025-05-25 10:30:00
published: true
---
<section class="gallery-page__gallery" style="padding-top:30px;">
<h2>Gallery</h2>
<div class="gallery-page__grid">
{% assign sorted = site.data.gallery | sort: "id" %}
{% for item in sorted %}
<div class="image-wrapper" data-url="{{ item.url }}"><img src="{{ item.url }}" alt="{{ item.title }}" loading="lazy" decoding="async" class="image"></div>
{% endfor %}
</div>
</section>
<div id="imageModal" class="modal" tabindex="-1" role="dialog" aria-modal="true"><img class="modal-content" id="modalImg"><div class="cnt"><div class="cnt-1"><button class="prev" aria-label="Previous image" title="Previous" type="button"><svg viewBox="0 0 24 24" style="display: none;" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"><path fill="none" d="M4 18l8-8 8 8" stroke="#fff7f9" stroke-width="3" stroke-linejoin="miter" /></svg>PREVIOUS</button><button class="next" aria-label="Next image" title="Next" type="button"><svg viewBox="0 0 24 24" style="display: none;" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"><path fill="none" d="M6 8l8 8 8-8" stroke="#fff7f9" stroke-width="3" stroke-linejoin="miter"/></svg>NEXT</button></div><button class="close" aria-label="Close modal" title="Close" type="button"><svg aria-hidden="true" style="display: none;" focusable="false" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 16 16"><path stroke="#fff7f9" stroke-width="2" d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"></path></svg>CLOSE</button></div></div>