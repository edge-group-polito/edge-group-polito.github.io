---
layout: default
title: Articles
permalink: /articles/
description: Notes, results and write-ups from the EDGE Group.
---

Notes, results and write-ups from the group.

<ul class="articles">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%-d %B %Y" }}</time>
    {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncate: 180 }}</p>{% endif %}
  </li>
{% else %}
  <li>Nothing published yet.</li>
{% endfor %}
</ul>
