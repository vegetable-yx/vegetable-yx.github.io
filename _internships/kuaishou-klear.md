---
layout: page
title: Kuaishou
description: Foundation Model Algorithm Intern, Klear Team · Feb 2026 – May 2026
importance: 2
category: graduate
logo: kuaishou.png # company logo — card top-right corner and this page
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

Foundation Model and Applications Department, Klear foundation model team.

#### Data System and Synthesis

- Decomposed and categorized 100+ high-quality novels along multiple dimensions, producing three reusable assets from the analysis: a taxonomy for novel data, a domain knowledge base, and a structured format specification.
- Built synthesis and quality filtering on top of that system, yielding roughly 6k high-quality post-training samples and expanding the pool of usable data by about 60x over what the raw corpus could supply directly.

#### Two-Stage Post-Training Paradigm

- Designed a two-stage Plan + Response data format and training paradigm that decouples planning from surface realization, turning the plan into an explicit, separately optimizable variable rather than a latent step buried inside one long generation.
- Built a chapter-by-chapter, multi-turn rewriting pipeline for long-form narrative, so consistency constraints are enforced incrementally instead of being left to a single pass over the whole text.
- Internal evaluation score rose from roughly 62 to 83 (+21), with format adherence above 98% and consistency above 95%.

#### Creative Writing RL

- Designed and validated Tree-Rollout RL on top of the two-stage framework: each plan is expanded into multiple responses, so a plan is scored by the expected return over its children instead of a single high-variance trajectory estimate, and the plan-level signal is propagated back down to those children.
- Improved on the contemporaneous SOTA approach by more than 5% across all four creative-writing benchmarks.
- Found that supervising the plan alone yields no gain — the credit has to reach the responses — which motivated the hierarchical credit assignment formulation developed further in my first-author submission to EMNLP 2026.
