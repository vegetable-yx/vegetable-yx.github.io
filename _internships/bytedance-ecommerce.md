---
layout: page
title: ByteDance
description: Algorithm Intern, Global E-commerce · Jan 2025 – Aug 2025
importance: 4
category: graduate
logo: # filename in assets/img/company/ — small logo in the card's top-right corner
# gallery: [bytedance-1.png, bytedance-2.png] # 1-2 pictures shown on the right of this page
---

{% if page.gallery %}
<div style="float: right; width: 16rem; max-width: 45%; margin: 0 0 1rem 1.5rem">
  {% for item in page.gallery %}
    {% assign gallery_image = item | prepend: "assets/img/internship/" %}
    {% include figure.liquid path=gallery_image class="img-fluid rounded z-depth-1" %}
  {% endfor %}
</div>
{% endif %}

#### Model Tuning

- Designed an uplift model to tune the traffic allocation algorithm behind product promotion, then optimized it end to end across model architecture, feature engineering, and data processing.
- Break-0 and break-5 product counts both rose 2.63%, with attainment rates up 4.72% and 0.52%; OPM of promoted products rose 23.32% and GPM rose 3.19%.

#### SAINT Transformer Productionization

- Independently handled training adaptation and prediction-task migration for SAINT Transformer on the company GPU cluster.
- Reached close to 80% accuracy on break-5 prediction for the top 10k products, roughly 5% above the baseline model.
