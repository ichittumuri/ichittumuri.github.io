---
title: "Fieldwork"
permalink: /fieldwork/
author_profile: true
classes: splash
header:
  overlay_image: https://ichittumuri.github.io/images/traverse.jpeg
---

<style>
.thumb-container {
  text-align: center;
  margin-bottom: 1em;
}

.thumb {
  max-width: 600px;
  width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
</style>

<div>
  {% for exp in site.data.fieldwork.repos %}
    <h2>{{ exp.title }}</h2>

    {% if exp.dates %}
      <p><strong>{{ exp.dates.start }} — {{ exp.dates.end }}</strong></p>
    {% endif %}

    {% if exp.image_path %}
      <div class="thumb-container">
        <img
          class="thumb"
          src="{{ exp.image_path | relative_url }}"
          alt="{{ exp.title }}"
        >
      </div>
    {% endif %}

    {{ exp.description | markdownify }}
    <hr>
  {% endfor %}
</div>
