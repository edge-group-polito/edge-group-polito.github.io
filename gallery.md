---
layout: default
title: Gallery
permalink: /gallery/
description: Photos from conferences and events organized or attended by the EDGE Group.
---

Photos from conferences, workshops and events involving the group.

{% assign years = site.data.gallery | group_by: "year" | sort: "name" | reverse %}
<div id="gallery">
{% for year in years %}
  <details class="pub-year"{% if forloop.first %} open{% endif %}>
    <summary class="pub-year-summary">{{ year.name }} <span class="pub-count">({{ year.items | size }})</span></summary>
    {% assign events = year.items | group_by: "event" %}
    {% for event in events %}
    <h3>{{ event.name }}</h3>
    <div class="grid gallery-grid">
      {% for p in event.items %}
      <a class="gallery-item" href="{{ '/photo/' | append: p.file | relative_url }}" target="_blank" rel="noopener">
        <img src="{{ '/photo/' | append: p.file | relative_url }}" alt="{{ event.name }}" loading="lazy">
      </a>
      {% endfor %}
    </div>
    {% endfor %}
  </details>
{% else %}
  <p>No photos yet.</p>
{% endfor %}
</div>
