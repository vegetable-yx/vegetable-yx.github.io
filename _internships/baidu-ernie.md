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

Selected for the ERNIE Rising Star top-talent program.

#### RL Training and Pipeline Governance

- Worked on Coding Agentic RL training for ERNIE Lite, covering reward modeling and the design of optimization objectives.
- Ran trajectory analysis, anomaly triage, and data diagnostics jointly with the Infra and algorithm teams, cutting the environment anomaly rate from roughly 8% to under 1%.

#### RL Algorithm Optimization

- Reworked advantage computation and loss backpropagation for trajectories under Context Management, along with sub-agent trajectory handling, improving training stability and effective sample utilization.
- Led the attribution and handling mechanism for abnormally terminated trajectories, substantially reducing reward hacking risk and wasted training compute.
- Raised the ERNIE Lite score on SWE-bench Verified from roughly 73 to 78.

#### Single-Step MOPD Training

- Derived the per-step mixing ratio of the training set from large volumes of production data, aligning the training distribution with the real step distribution.
- Mixed both teacher and student history into the training context to reduce bias from error accumulation.
- Redesigned the top-k selection strategy while holding K at parity with the original scheme, so compute cost stayed essentially unchanged; the resulting balance of efficiency and effectiveness lifted final scores by roughly 5% on average.
