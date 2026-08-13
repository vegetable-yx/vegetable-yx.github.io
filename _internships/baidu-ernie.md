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

Coding Agentic RL for ERNIE Lite — reward modeling, optimization objectives, trajectory governance, and single-step distillation training.

#### Advantage Attribution and Loss Backpropagation

Under Context Management a trajectory is not a homogeneous token stream: the context the policy conditions on interleaves tokens the policy produced itself, tokens injected by the environment (tool returns, compiler and test output, retrieved files), and tokens rewritten by summarization when the window is compacted. Treating all of them as policy actions leaks gradient into text the model never chose.

- Partitioned each trajectory by token provenance — policy-generated, environment-injected, summary-rewritten — and derived a token-level loss mask from that partition, so gradient reaches only policy-generated tokens while the rest stay pure conditioning context.
- Re-derived advantage attribution on the same partition, keeping the advantage aligned with the decisions the policy is actually accountable for instead of diluting it across injected content.
- Handled sub-agent trajectories explicitly: a sub-agent rollout carries no independent outcome reward, so it inherits advantage from the parent trajectory's outcome, keeping its contribution inside the same objective rather than dropping it from optimization.
- Improved training stability and effective sample utilization, raising the ERNIE Lite score on SWE-bench Verified from roughly 73 to 78.

#### Reward Hacking Mitigation

- Built a rules-first detection layer for known hacking patterns — test tampering, weakened assertions, hard-coded expected outputs, bypassing the harness — and fell back to an LLM judge only for cases the rules cannot decide, keeping both cost and false-positive rate controlled.
- Localized the first violating step instead of penalizing the trajectory as a whole, so the penalty is temporally aligned with the offending action and the useful signal accumulated before the violation is preserved rather than discarded.

#### Trajectory Attribution and Environment Governance

- Ran trajectory analysis, anomaly triage, and data diagnostics jointly with the Infra and algorithm teams, cutting the environment anomaly rate from roughly 8% to under 1%.
- Designed the attribution mechanism for abnormally terminated trajectories: each termination is attributed to the environment or to the policy, then routed to one of three treatments — discarded, masked out of the loss, or penalized — so infrastructure faults are never charged to the policy while genuine policy failures still are.
- Substantially reduced reward hacking risk and wasted training compute.

#### Single-Step MOPD Training

- Estimated the per-step mixing ratio of the training set from large volumes of production data, aligning the training-time step distribution with the real step distribution observed in serving instead of a hand-set uniform prior.
- Mixed both teacher and student history into the training context, so the model is optimized under the error-accumulated states it actually meets at inference and exposure bias is reduced.
- Rebuilt the top-k selection strategy while holding K at parity with the original scheme, leaving compute cost essentially unchanged; the resulting efficiency/quality balance lifted final scores by roughly 5% on average.
