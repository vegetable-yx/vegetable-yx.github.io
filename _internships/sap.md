---
layout: page
title: SAP
description: Software Development Intern · 2023
importance: 6
category: undergraduate
logo: sap.png # company logo — card top-right corner and this page
team_logo: # optional team/department logo — this page only
---

{% if page.logo or page.team_logo %}
<div style="float: right; margin: 0 0 1rem 1.5rem; text-align: center">
  {% if page.logo %}
    <img src="{{ page.logo | prepend: '/assets/img/company/' | relative_url }}" alt="{{ page.title }}" style="display: block; max-height: 4.5rem; max-width: 12rem; margin: 0 auto 1rem" />
  {% endif %}
  {% if page.team_logo %}
    <img src="{{ page.team_logo | prepend: '/assets/img/company/' | relative_url }}" alt="{{ page.title }} team" style="display: block; max-height: 4.5rem; max-width: 12rem; margin: 0 auto" />
  {% endif %}
</div>
{% endif %}

Android application development, contributing features and fixes alongside the product engineering team.
