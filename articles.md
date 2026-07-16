---
layout: default
title: Articles
permalink: /articles/
description: Papers and articles published by the EDGE Group.
---

Papers and articles published by the group. Click a box to read the abstract.

<ul class="publications">
{% for post in site.posts %}
  <li class="pub">
    <details class="pub-main">
      <summary>
        <span class="pub-title">{{ post.title }}</span>
        {% if post.authors %}<span class="pub-authors">{{ post.authors }}</span>{% endif %}
        {% if post.citation %}<span class="pub-citation">{{ post.citation }}</span>{% endif %}
      </summary>
      <div class="pub-abstract">{{ post.content }}</div>
    </details>
    {% if post.paper_url or post.repo_url %}
    <div class="pub-links">
      {% if post.paper_url %}<a href="{{ post.paper_url }}" target="_blank" rel="noopener">Paper ↗</a>{% endif %}
      {% if post.repo_url %}<a href="{{ post.repo_url }}" target="_blank" rel="noopener">Repository ↗</a>{% endif %}
    </div>
    {% endif %}
  </li>
{% else %}
  <li>Nothing published yet.</li>
{% endfor %}
</ul>
