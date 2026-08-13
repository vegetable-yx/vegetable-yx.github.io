---
layout: page
title: Baidu
description: Foundation Model Algorithm Intern, ERNIE Team · May 2026 – Present
importance: 1
category: graduate
logo: baidu.png # company logo — card top-right corner and this page
team_logo: ernie.png # optional team/department logo — this page only
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

Selected for the **ERNIE Rising Star Top-Talent Program**.

Agentic reinforcement learning for coding on the ERNIE Lite model.

- **Reward Modeling and Optimization Objective Design**
- **Credit Assignment for Long-Horizon Agentic Trajectories**
- **Reward Hacking Governance and Trajectory Attribution**
- **Single-Step Distillation Training at Production Scale**
