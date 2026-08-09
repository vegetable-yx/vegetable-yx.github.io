---
layout: page
title: Internships
permalink: /internships/
description: Industry internships and research experience.
nav: true
nav_order: 3
---

<style>
  h1 {
    text-transform: uppercase;
  }
</style>

<!--
  _pages/internships.md — entries live in _internships/, grouped by their `category`
  field (`graduate` / `undergraduate`) and ordered within a group by `importance`.
  Set `logo: <filename>` in an entry to show a small logo in the card's top-right
  corner; the file goes in assets/img/company/.
-->

<div class="projects">
{% assign groups = "graduate,undergraduate" | split: "," %}
{% assign rendered = 0 %}
{% for group in groups %}
  {% assign items = site.internships | where: "category", group | sort: "importance" %}
  {% if items.size > 0 %}
    {% if rendered > 0 %}<hr />{% endif %}
    <h2 class="category">{{ group | capitalize }}</h2>
    <div class="row row-cols-1 row-cols-md-3">
      {% for project in items %}
        <div class="col mb-4">
          <a href="{{ project.url | relative_url }}">
            <div class="card hoverable" style="position: relative; height: 100%">
              {% if project.logo %}
                <img
                  src="{{ project.logo | prepend: '/assets/img/company/' | relative_url }}"
                  alt="{{ project.title }}"
                  style="position: absolute; top: 1rem; right: 1rem; height: 1.6rem; max-width: 5.5rem; object-fit: contain; object-position: right center"
                />
              {% endif %}
              <div class="card-body" style="{% if project.logo %}padding-right: 6.5rem{% endif %}">
                <h2 class="card-title">{{ project.title }}</h2>
                <p class="card-text">{{ project.description }}</p>
              </div>
            </div>
          </a>
        </div>
      {% endfor %}
    </div>
    {% assign rendered = rendered | plus: 1 %}
  {% endif %}
{% endfor %}
</div>
