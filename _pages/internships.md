---
layout: page
title: internships
permalink: /internships/
description: Industry internships and research experience.
nav: true
nav_order: 3
horizontal: false
---

<!-- _pages/internships.md — entries live in _internships/, grouped by their `category` field -->

<div class="projects">

{% assign graduate = site.internships | where: "category", "graduate" | sort: "importance" %}
{% assign undergraduate = site.internships | where: "category", "undergraduate" | sort: "importance" %}

{% if graduate.size > 0 %}
  <h2 class="category">Graduate</h2>
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in graduate %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in graduate %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}

{% if graduate.size > 0 and undergraduate.size > 0 %}
  <hr />
{% endif %}

{% if undergraduate.size > 0 %}
  <h2 class="category">Undergraduate</h2>
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in undergraduate %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in undergraduate %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}

</div>
