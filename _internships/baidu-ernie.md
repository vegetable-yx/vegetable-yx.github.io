---
layout: page
title: Baidu
description: Foundation Model Algorithm Intern, ERNIE Team · May 2026 – Present
importance: 1
---

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
