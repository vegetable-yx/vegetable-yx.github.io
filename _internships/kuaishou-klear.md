---
layout: page
title: Kuaishou
description: Foundation Model Algorithm Intern, Klear Team · Feb 2026 – May 2026
importance: 2
category: graduate
logo: # filename in assets/img/company/ — small logo in the card's top-right corner
# gallery: [kuaishou-1.png, kuaishou-2.png] # 1-2 pictures shown on the right of this page
---

{% if page.gallery %}
<div style="float: right; width: 16rem; max-width: 45%; margin: 0 0 1rem 1.5rem">
  {% for item in page.gallery %}
    {% assign gallery_image = item | prepend: "assets/img/internship/" %}
    {% include figure.liquid path=gallery_image class="img-fluid rounded z-depth-1" %}
  {% endfor %}
</div>
{% endif %}

Foundation Model and Applications Department, Klear foundation model team.

#### Data Pipeline and Synthesis

- Decomposed and categorized 100+ high-quality novels along multiple dimensions, producing a taxonomy for novel data, a domain knowledge base, and a structured format specification.
- Built data synthesis and quality filtering on top of that system, yielding roughly 6k high-quality post-training samples and expanding the pool of usable data by about 60x.

#### Novel Base Model Training

- Designed a two-stage Plan + Response data format and training paradigm, plus a chapter-by-chapter, multi-turn rewriting pipeline for long-form narrative.
- Internal evaluation score rose from roughly 62 to 83 (+21), with format adherence above 98% and consistency above 95%.

#### Creative Writing RL

- Designed and validated a Tree-Rollout RL training scheme for creative writing on top of the two-stage generation framework.
- Improved on the contemporaneous SOTA approach by more than 5% across all four creative-writing benchmarks. Submitted to EMNLP 2026.
