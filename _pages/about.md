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

My research aims to build agents that make **robust decisions in the real world and on frontier tasks**, where deployment rarely matches training. I work along three connected directions: **robust reinforcement learning**, with algorithms and benchmarks for policies under shifts in dynamics, observations, actions, rewards, latency and task semantics; **generative models for decision-making**, which represent plausible uncertainty and synthesize experience for data-efficient learning; and **embodied and multi-agent systems**, carrying these methods to robot learning, sim-to-real transfer and LLM-based multi-agent collaboration.

I am **applying for a Ph.D.** to pursue this agenda, and I'm always happy to connect about research or collaborations.

---

## news

{% include news.liquid limit=true %}

## selected research projects

**RobustRLlib: A Unified Library and Benchmark for Robust Reinforcement Learning Algorithms** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span><br>
_Project lead, Johns Hopkins University — with Prof. Laixi Shi_ · [Project page](https://robustrl-lib.github.io/) · [GitHub](https://github.com/robustrl-lib/robustrllib)

- Designed and built an algorithm-centric library of **23 standard and robust online, offline and safe RL algorithms**, organized by robustness mechanism and claimed shift, each trained with its native recipe and scored under one train–disrupt–evaluate protocol.
- Built a composable shift toolbox of **six deployment-facing sources** (dynamics, observation, action, reward/cost, control latency, scene semantics) and five modes (parametric, stochastic, scheduled, adversarial, compound), evaluated across **273 perturbation configurations** on MuJoCo, Box2D and robosuite tasks.
- Produced an up-to-date **capability map** of robust RL: a method's claimed shift does not fully predict its empirical strengths, the shift it covers changes with task and severity, and robust methods lift the degradation curve without moving the point where it collapses.
- Extended the same interface to Isaac Lab (Unitree G1 humanoid locomotion and Franka drawer manipulation, with robust safe RL baselines) and a frozen vision–language–action policy to mimic the sim-to-real gap.

**Leveraging Generative Uncertainty Modeling for Distributionally Robust Offline Reinforcement Learning** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span><br>
_Johns Hopkins University — with Prof. Laixi Shi, Prof. Jianyi Yang and Jiaqi Wen_ · <span style="color: var(--global-text-color-light)">Under review</span>

- A plug-in robust target-generation framework for offline RL: a conditional flow model defines a trajectory-level, **non-rectangular uncertainty set**, with the flow-matching loss as the discrepancy measure, which implies a Wasserstein-2 bound to the offline data.
- Implemented policy-aware **adversarial fine-tuning of the flow world model** (inverse-propensity-weighted value degradation, PPO-clipped surrogate, primal–dual flow-matching constraint) that generates adverse _H_-step critic targets for IQL, CQL and BCQ backbones.
- Achieved the best OOD score across six MuJoCo task–dataset settings, **+6.7 normalized points** over the strongest baseline, with gains on all three backbones and an EPANET water-network control case study.

**Track-Any-Point Foundation Model for Endoscopic Scenes** &nbsp; <span style="color: var(--global-text-color-light)">· Feb 2026 – Present</span><br>
_ARCADE Lab, Johns Hopkins University — with Dr. Lalithkumar Seenivasan_ · <span style="color: var(--global-text-color-light)">Manuscript in preparation</span>

- Extended AllTracker with a **dual-correlation** design that fuses long-range anchor correspondence with flow-aligned adjacent-frame matching for bronchoscopy, where textureless anatomy, specular reflections, deformation and rapid camera motion break existing trackers; reaches **91.9% δ<sub>avg</sub>**, above the anchor-only baseline.
- Designed a cosine-gated **feature memory** that refreshes per-point appearance templates, cutting invisible-point loss by ~9% for recovery from occlusion and re-entry.
- Optimized sliding-window inference with feature reuse for real-time throughput (~120–156 fps, ~0.4 GB memory).

**Backdoor Attacks on Multivariate Time Series Forecasting with Missing Values** &nbsp; <span style="color: var(--global-text-color-light)">· Dec 2024 – May 2025</span><br>
_Undergraduate thesis, DBIS Lab, Nankai University — with Dr. Xiangrui Cai_

- Developed a backdoor-attack framework for forecasting under realistic missing values, where prior attacks assume complete inputs and struggle to be both effective and stealthy.
- Designed a critical-time-step-guided imputation strategy and dynamic trigger placement driven by missing-value density, prediction sensitivity and local volatility.
- Achieved **17–43%** relative improvement over baseline attack strategies on PeMS traffic datasets.
