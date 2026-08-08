---
layout: page
title: honors
permalink: /honors/
description: Scholarships, fellowships, and other honors.
nav: true
nav_order: 4
---

<!-- _pages/honors.md — edit the entries in _data/honors.yml, not this file -->

{% assign honors = site.data.honors %}
{% if honors and honors.size > 0 %}

<ul class="list-honors">
  {% for item in honors %}
  <li>
    {% if item.url %}<a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.title }}</a>{% else %}<strong>{{ item.title }}</strong>{% endif %}
    {% if item.issuer %}&middot; {{ item.issuer }}{% endif %}
    {% if item.date %}&middot; {{ item.date }}{% endif %}
    {% if item.summary %}<div class="text-muted">{{ item.summary }}</div>{% endif %}
  </li>
  {% endfor %}
</ul>

{% else %}

Nothing listed yet — add entries to `_data/honors.yml`.

{% endif %}
