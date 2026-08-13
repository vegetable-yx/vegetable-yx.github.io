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

#### Uplift Traffic Allocation Modeling

- Designed an uplift model for the traffic allocation algorithm behind product promotion, then optimized it end to end across model architecture, feature engineering, and data processing.
- Independently handled training adaptation and prediction-task migration for a SAINT-style Transformer on the company GPU cluster, taking it from research setup to a production training and inference path.
- Break-0 and break-5 product counts both rose 2.63%, with attainment rates up 4.72% and 0.52%; OPM of promoted products rose 23.32% and GPM rose 3.19%.
- Reached close to 80% accuracy on break-5 prediction for the top 10k products, roughly 5% above the baseline model.
