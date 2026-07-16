---
layout: default
title: Posts
permalink: /posts/
description: Updates and news from the EDGE Group.
---

Updates from the group — also posted on our
<a href="https://www.linkedin.com/company/edgevlsi/">LinkedIn page</a>.

{% assign sorted = site.updates | sort: "date" | reverse %}
{% assign years = sorted | group_by_exp: "post", "post.date | date: '%Y'" %}
<div id="feed">
{% for year in years %}
  <details class="pub-year"{% if forloop.first %} open{% endif %}>
    <summary class="pub-year-summary">{{ year.name }} <span class="pub-count">({{ year.items | size }})</span></summary>
    <ul class="feed-list">
    {% for post in year.items %}
      <li class="feed-post">
        <div class="feed-header">
          <img class="feed-avatar" src="{{ '/assets/img/logo.png' | relative_url }}" alt="">
          <div>
            <span class="feed-name">EDGE Group</span>
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %Y" }}</time>
          </div>
        </div>
        <div class="feed-body">
          {{ post.content }}
        </div>
        {% if post.photos %}
        <div class="feed-photos">
          {% for photo in post.photos %}
          <img src="{{ photo | relative_url }}" alt="">
          {% endfor %}
        </div>
        {% endif %}
        {% if post.link %}
        <a class="feed-link" href="{{ post.link }}" target="_blank" rel="noopener">{{ post.link_label | default: "Read more ↗" }}</a>
        {% endif %}
      </li>
    {% endfor %}
    </ul>
  </details>
{% else %}
  <p>Nothing posted yet.</p>
{% endfor %}
</div>
