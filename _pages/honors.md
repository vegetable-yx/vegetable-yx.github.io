---
layout: page
title: Honors
permalink: /honors/
description: Scholarships, fellowships, and other honors.
nav: true
nav_order: 4
---

<style>
  h1 {
    text-transform: uppercase;
  }
</style>

<!-- _pages/honors.md — edit the entries in _data/honors.yml, not this file -->

{% assign honors = site.data.honors %}
{% if honors and honors.size > 0 %}

<ul class="list-honors">
  {% for item in honors %}
  <li style="margin-bottom: 1rem">
    {% if item.url %}<a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.title }}</a>{% else %}<strong>{{ item.title }}</strong>{% endif %}
    {% if item.issuer %}&middot; {{ item.issuer }}{% endif %}
    {% if item.date %}&middot; {{ item.date }}{% endif %}
    {% if item.summary %}<div class="text-muted">{{ item.summary }}</div>{% endif %}
    {% if item.images %}
      {% for file in item.images %}
        {% if file contains ".pdf" %}
          <div style="margin-top: 0.25rem">
            <a href="{{ file | prepend: '/assets/img/honor/' | relative_url }}" target="_blank" rel="noopener">Certificate (PDF)</a>
          </div>
        {% else %}
          {% assign honor_image = file | prepend: "assets/img/honor/" %}
          <div style="margin-top: 0.5rem; max-width: 22rem">
            {% include figure.liquid path=honor_image class="img-fluid rounded z-depth-1" title=item.title %}
          </div>
        {% endif %}
      {% endfor %}
    {% endif %}
  </li>
  {% endfor %}
</ul>

{% else %}

Nothing listed yet — add entries to `_data/honors.yml`.

{% endif %}
