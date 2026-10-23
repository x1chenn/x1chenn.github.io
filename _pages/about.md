---
layout: about
title: about
permalink: /
subtitle: M.S.E. in Computer Science @ <a href='https://www.jhu.edu/'>Johns Hopkins University</a> | Robust RL · Robot Learning · Generative Models

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Department of Computer Science</p>
    <p>Johns Hopkins University</p>
    <p>Baltimore, MD, USA</p>

selected_papers: false # I have no publications yet; research projects are listed in the body instead
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # rendered manually in the body, above the research projects
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true
  limit: 3
---

Hi! I'm **Xi Chen (陈希)**, a second-year **M.S.E. student in Computer Science** at **Johns Hopkins University**. I am fortunate to be advised by [Prof. Laixi Shi](https://laixishi.github.io/index.html)! Before JHU, I received my B.Eng. in Computer Science from **Nankai University**.

My research aims to build agents that make **reliable decisions in the real world and on frontier tasks**, where deployment rarely matches training. I work along three lines:

1. **Robust decision-making under deployment shift** — robust RL that makes better decisions under deployment disruptions, including generative models that represent plausible shifts.
2. **Systems for reliable agents** — turning realistic problems, from deployment shifts to multi-agent coordination, into reusable platforms and benchmarks that reveal where agents succeed and fail.
3. **Sim-to-real deployment** — carrying robust policies, from RL controllers to vision–language–action models, onto real robots, and letting deployment failures guide algorithm design.

I am **applying for a Ph.D.** to pursue this agenda, and I'm always happy to connect about research or collaborations.

---

## news

{% include news.liquid limit=true %}

## selected research projects

**RobustRLlib: A Unified Library and Benchmark for Robust Reinforcement Learning Algorithms** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span><br>
_Project lead, Johns Hopkins University — with Prof. Laixi Shi_ · [Project page](https://robustrl-lib.github.io/) · [GitHub](https://github.com/robustrl-lib/robustrllib)

- **Algorithm library**: 17 robust online, offline and safe RL algorithms plus 6 standard baselines under one unified interface, organized by algorithm feature, claimed target shift and base algorithm.
- **Disruptor toolbox**: six shift sources (MDP elements, latency, semantics) and five shift modes (stochastic, adversarial, parametric, non-stationary, composition), isolated or compound.
- **Capability map** over 273 perturbation configurations: robust RL leads on average but degrades as shifts intensify, and a claimed target shift does not reliably predict empirical strengths.
- Extended the same interface to advanced robotic tasks: Unitree G1 and Franka drawer in Isaac Lab with robust safe RL, and a fine-tuned π<sub>0.5</sub> VLA policy.

**Leveraging Generative Uncertainty Modeling for Distributionally Robust Offline Reinforcement Learning** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span><br>
_Johns Hopkins University — with Prof. Laixi Shi, Prof. Jianyi Yang and Jiaqi Wen_ · <span style="color: var(--global-text-color-light)">Under review</span>

- A non-rectangular, trajectory-level **uncertainty set built from a conditional flow model**, with the flow-matching loss as a tractable discrepancy that implies a Wasserstein bound.
- Implemented **adversarial fine-tuning of the flow world model** within this set; its adverse multi-step trajectories augment conservative offline value learning on IQL, CQL and BCQ.
- Best OOD score on six MuJoCo task–dataset settings (**+6.7** normalized points over the strongest baseline), with gains on an EPANET water-network case study.

**Track-Any-Point Foundation Model for Endoscopic Scenes** &nbsp; <span style="color: var(--global-text-color-light)">· Feb 2026 – Present</span><br>
_ARCADE Lab, Johns Hopkins University — with Dr. Lalithkumar Seenivasan_ · <span style="color: var(--global-text-color-light)">Manuscript in preparation</span>

- Extended AllTracker with **dual correlation** (long-range anchors plus flow-aligned adjacent frames) for bronchoscopy, reaching **91.9% δ<sub>avg</sub>**, above the anchor-only baseline.
- Added a cosine-gated **feature memory** that cuts invisible-point loss by ~9%, and sliding-window inference with feature reuse at ~120–156 fps.

**Backdoor Attacks on Multivariate Time Series Forecasting with Missing Values** &nbsp; <span style="color: var(--global-text-color-light)">· Dec 2024 – May 2025</span><br>
_Undergraduate thesis, DBIS Lab, Nankai University — with Dr. Xiangrui Cai_

- A backdoor attack for forecasting under missing values, where prior attacks assume complete inputs and struggle to be both effective and stealthy.
- Critical-time-step-guided imputation and dynamic trigger placement give **17–43%** relative improvement over baseline attacks on PeMS traffic data.
