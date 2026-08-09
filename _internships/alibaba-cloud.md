---
layout: page
title: Alibaba
description: Algorithm Intern, Alibaba Cloud · 2023 – 2024
importance: 5
category: undergraduate
logo: # filename in assets/img/company/ — small logo in the card's top-right corner
# gallery: [alibaba-1.png, alibaba-2.png] # 1-2 pictures shown on the right of this page
---

{% if page.gallery %}
<div style="float: right; width: 16rem; max-width: 45%; margin: 0 0 1rem 1.5rem">
  {% for item in page.gallery %}
    {% assign gallery_image = item | prepend: "assets/img/internship/" %}
    {% include figure.liquid path=gallery_image class="img-fluid rounded z-depth-1" %}
  {% endfor %}
</div>
{% endif %}

Worked on LLM reasoning, exploring approaches for improving multi-step reasoning quality and evaluating them against internal benchmarks.
