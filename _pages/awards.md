---
layout: page
title: Awards
permalink: /awards/
description: Paper awards and competition results.
nav: true
nav_order: 5
---

<style>
  h1 {
    text-transform: uppercase;
  }
</style>

<!-- _pages/awards.md — edit the entries in _data/awards.yml, not this file -->

{% assign awards = site.data.awards %}
{% if awards and awards.size > 0 %}

<ul class="list-awards">
  {% for item in awards %}
  <li style="margin-bottom: 1rem">
    {% if item.url %}<a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.title }}</a>{% else %}<strong>{{ item.title }}</strong>{% endif %}
    {% if item.awarder %}&middot; {{ item.awarder }}{% endif %}
    {% if item.date %}&middot; {{ item.date }}{% endif %}
    {% if item.summary %}<div class="text-muted">{{ item.summary }}</div>{% endif %}
    {% if item.image %}
      {% assign award_image = item.image | prepend: "assets/img/award/" %}
      <div style="margin-top: 0.5rem; max-width: 22rem">
        {% include figure.liquid path=award_image class="img-fluid rounded z-depth-1" title=item.title %}
      </div>
    {% endif %}
  </li>
  {% endfor %}
</ul>

{% else %}

Nothing listed yet — add entries to `_data/awards.yml`.

{% endif %}
