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
{% for item in sorted %}
<div class="image-wrapper" data-url="{{ item.url }}">
<img src="{{ item.url }}" alt="{{ item.title }}" loading="lazy" decoding="async" class="image">
</div>
{% endfor %}
</div>
</div>
</section>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const modal = document.getElementById("imageModal");
  const modalImg = document.getElementById("modalImg");
  const closeBtn = document.querySelector(".close");

  document.querySelectorAll(".image-wrapper").forEach(wrapper => {
    wrapper.addEventListener("click", function () {
      modal.style.display = "block";
      modalImg.src = this.dataset.url;
    });
  });

  closeBtn.onclick = function () {
    modal.style.display = "none";
    modalImg.src = "";
  };

  window.onclick = function (e) {
    if (e.target === modal) {
      modal.style.display = "none";
      modalImg.src = "";
    }
  };
});
</script>