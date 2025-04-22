---
title: "Workshops"
permalink: /workshops/
author_profile: true
classes: splash
header:
  overlay_image: https://ichittumuri.github.io/images/taku_towers.jpg
---

<div>
  {% for exp in site.data.workshops.repos %}
    <h2>{{ exp.title }}</h2>

    {% if exp.dates %}
      <p><strong>{{ exp.dates.start }} — {{ exp.dates.end }}</strong></p>
    {% endif %}

    <p>{{ exp.description | markdownify }}</p>
    <hr>
  {% endfor %}
</div>
