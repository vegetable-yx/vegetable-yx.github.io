---
layout: page
title: Meituan
description: LLM Algorithm Intern, LongCat Interaction · Aug 2025 – Feb 2026
importance: 3
category: graduate
logo: meituan.png # company logo — card top-right corner and this page
team_logo: longcat.png # optional team/department logo — this page only
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

#### WOWService

- Contributed to an intelligent interaction system built on LLM tuning and multi-agent collaboration, now deployed at scale in the Meituan app and documented in a published technical report.
- Owned the design and engineering of the end-to-end DPO training pipeline — preference pair construction, filtering, training, and offline/online evaluation — lifting performance across 8 core issue scenarios by roughly 11% on average over the pre-training baseline.

#### Post-Training Robustness

- Systematically analyzed model stability under several classes of perturbation, then proposed a post-training method that improves robustness without trading away task accuracy.
- Gained roughly 5% and 2% over SOTA on LLaMA and Qwen 7B respectively, with gains of roughly 4% and 3% holding in Qwen 14B and 72B scaling experiments.
- The method was written up as my first-author ICLR paper, CoIPO.

#### Dynamic Data Mixing

- Ported the ADO dynamic data-mixing algorithm to the company's Megatron-based training framework, planning the next batch's data distribution online from task category and current training state.
- Turned the data mixture from a pre-set hyperparameter into an online decision variable, improving overall model performance by roughly 5% on average with training data and model architecture held constant.

#### Enterprise Knowledge Assistant

- Independently built an enterprise knowledge agent on the internal platform, combining knowledge-base QA, document retrieval, and summarization.
- Rolled out for daily use across a large team, serving 200+ internal calls per day and cutting repeated search and document cleanup work.

#### Enterprise Knowledge Assistant

- Independently built an enterprise knowledge agent on the internal platform, combining knowledge-base QA, document retrieval, and summarization.
- Rolled out for daily use across a large team, serving 200+ internal calls per day and cutting repeated search and document cleanup work.
