---
title: "Field Work"
permalink: /fieldwork/
author_profile: true
classes: splash
header:
  overlay_image: https://ichittumuri.github.io/images/traverse.jpg
---

<div>
  {% for exp in site.data.fieldwork.repos %}
    <h2>{{ exp.title }}</h2>

    {% if exp.dates %}
      <p><strong>{{ exp.dates.start }} — {{ exp.dates.end }}</strong></p>
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

    <p>{{ exp.description | markdownify }}</p>
    <hr>
  {% endfor %}
</div>
