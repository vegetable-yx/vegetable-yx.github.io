---
layout: page
title: SAP
description: Software Development Intern · 2023
importance: 6
category: undergraduate
logo: # filename in assets/img/company/ — small logo in the card's top-right corner
# gallery: [sap-1.png, sap-2.png] # 1-2 pictures shown on the right of this page
---

{% if page.gallery %}
<div style="float: right; width: 16rem; max-width: 45%; margin: 0 0 1rem 1.5rem">
  {% for item in page.gallery %}
    {% assign gallery_image = item | prepend: "assets/img/internship/" %}
    {% include figure.liquid path=gallery_image class="img-fluid rounded z-depth-1" %}
  {% endfor %}
</div>
{% endif %}

Android application development, contributing features and fixes alongside the product engineering team.
