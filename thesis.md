---
layout: default
title: Thesis
permalink: /thesis/
description: Thesis proposals and thesis students of the EDGE Group.
---

## Thesis proposals

Open Bachelor's/Master's thesis topics with the group.

<ul class="thesis-proposals">
{% for p in site.data.thesis_proposals %}
  <li class="proposal">
    <span class="proposal-title">{{ p.title }}</span>
    {% if p.advisor %}<span class="proposal-advisor">{{ p.advisor }}</span>{% endif %}
    {% if p.description %}<p>{{ p.description }}</p>{% endif %}
  </li>
{% else %}
  <li>No open proposals right now — check back soon.</li>
{% endfor %}
</ul>

## Thesis students

{% assign theses = site.data.theses | sort: "year" | reverse %}
<ul class="thesis-list">
{% for t in theses %}
  <li class="thesis-entry">
    <span class="thesis-student">{{ t.student }}</span>
    <span class="thesis-title">{{ t.title }}</span>
    {% if t.link %}<a class="thesis-link" href="{{ t.link }}" target="_blank" rel="noopener">Thesis ↗</a>{% endif %}
  </li>
{% else %}
  <li>Nothing published yet.</li>
{% endfor %}
</ul>
