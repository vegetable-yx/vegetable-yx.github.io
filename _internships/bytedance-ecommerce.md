---
layout: page
title: ByteDance
description: Algorithm Intern, Global E-commerce · Jan 2025 – Aug 2025
importance: 4
category: graduate
logo: bytedance.png # company logo — card top-right corner and this page
team_logo: tt.png # optional team/department logo — this page only
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

Traffic allocation modeling for global e-commerce product promotion.

- **Uplift Modeling for Traffic Allocation**
- **Transformer-Based Sequential Prediction in Production**
