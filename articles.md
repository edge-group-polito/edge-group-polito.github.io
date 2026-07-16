---
layout: default
title: Articles
permalink: /articles/
description: Papers and articles published by the EDGE Group.
---

Papers and articles published by the group. Click a box to read the abstract.

<div class="pub-search">
  <input type="search" id="pub-search" placeholder="Search by author or title…" aria-label="Search articles by author or title">
</div>

{% assign years = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
<div id="publications">
{% for year in years %}
  <details class="pub-year"{% if forloop.first %} open{% endif %}>
    <summary class="pub-year-summary">{{ year.name }} <span class="pub-count">({{ year.items | size }})</span></summary>
    <ul class="publications">
    {% for post in year.items %}
      <li class="pub" data-title="{{ post.title | downcase | escape }}" data-authors="{{ post.authors | downcase | escape }}">
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
          {% if post.paper_url %}
          <a href="{{ post.paper_url }}" target="_blank" rel="noopener" title="Paper" aria-label="Paper">
            <img src="{{ '/assets/img/logo.png' | relative_url }}" alt="Paper" class="pub-icon invert-on-light">
          </a>
          {% endif %}
          {% if post.repo_url %}
          <a href="{{ post.repo_url }}" target="_blank" rel="noopener" title="Repository" aria-label="Repository">
            <img src="{{ '/assets/img/github.png' | relative_url }}" alt="Repository" class="pub-icon invert-on-dark">
          </a>
          {% endif %}
        </div>
        {% endif %}
      </li>
    {% endfor %}
    </ul>
  </details>
{% else %}
  <p>Nothing published yet.</p>
{% endfor %}
</div>
<p id="pub-empty" hidden>No articles match your search.</p>

<script>
(function () {
  var input = document.getElementById('pub-search');
  var yearGroups = document.querySelectorAll('.pub-year');
  var empty = document.getElementById('pub-empty');
  if (!input || !yearGroups.length) return;

  yearGroups.forEach(function (group) { group.dataset.defaultOpen = group.open; });

  input.addEventListener('input', function () {
    var q = input.value.trim().toLowerCase();
    var anyVisible = false;

    yearGroups.forEach(function (group) {
      var groupHasMatch = false;
      group.querySelectorAll('.pub').forEach(function (pub) {
        var match = !q || pub.dataset.title.indexOf(q) !== -1 || pub.dataset.authors.indexOf(q) !== -1;
        pub.hidden = !match;
        if (match) groupHasMatch = true;
      });
      group.hidden = !groupHasMatch;
      group.open = q ? groupHasMatch : (group.dataset.defaultOpen === 'true');
      if (groupHasMatch) anyVisible = true;
    });

    empty.hidden = !(q && !anyVisible);
  });
})();
</script>
