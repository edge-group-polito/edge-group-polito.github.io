---
layout: default
title: Gallery
permalink: /gallery/
description: Photos from conferences and events organized or attended by the EDGE Group.
---

Photos from conferences, workshops and events involving the group.

{% assign events = site.data.gallery | group_by: "event" %}
{% for event in events %}
## {{ event.name }}

<div class="grid gallery-grid">
  {% for p in event.items %}
  <a class="gallery-item" href="{{ '/photo/' | append: p.file | relative_url }}" target="_blank" rel="noopener">
    <img src="{{ '/photo/' | append: p.file | relative_url }}" alt="{{ event.name }}" loading="lazy">
  </a>
  {% endfor %}
</div>
{% else %}
No photos yet.
{% endfor %}
