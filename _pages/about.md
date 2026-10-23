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

My research aims to build capable agents that make **robust decisions in the real world and on frontier tasks**, where deployment rarely looks like training. I approach this along three directions:

1. 🛡️ **Robust reinforcement learning** — algorithms that keep policies reliable under shifts in dynamics, observations, actions, rewards, latency and task semantics, and benchmarks that measure such robustness fairly.
2. 🌍 **Generative models for decision-making** — generative models that represent plausible uncertainty and synthesize experience, so that agents learn from limited data and prepare for the futures they may face.
3. 🤖 **Embodied and multi-agent systems** — carrying these methods to robot learning and sim-to-real transfer, and to LLM-based multi-agent systems that must cooperate reliably with each other and with people.

Earlier work spans time-series learning, generative modeling and computer vision. I am **applying for a Ph.D.** to pursue this agenda, and I'm always happy to connect — feel free to reach out about research or collaborations.

---

## news

{% include news.liquid limit=true %}

## selected research projects

**RobustRLlib: A Unified Library and Benchmark for Robust Reinforcement Learning Algorithms** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span>

_Johns Hopkins University — with Prof. Laixi Shi and collaborators_

An algorithm-centric library and benchmark for robust RL under deployment uncertainty. It integrates **22 algorithms** (6 standard, 16 robust online, offline and safe), organizes them by mechanism and claimed uncertainty, and evaluates every frozen policy under one protocol on a **shift toolbox of six sources** (dynamics, observation, action, reward/cost, latency, semantic) with several modes and their compositions, across hundreds of perturbation configurations. The same interface runs on advanced robotic tasks — humanoid and manipulation in Isaac Lab and a frozen vision–language–action policy — to mimic the sim-to-real gap. The findings: robustness is channel-specific, and a method's claimed channel does not fully predict where it is strongest.
<span style="color: var(--global-text-color-light)">_Under review. Library and project website to be released after the review period._</span>

**Leveraging Generative Uncertainty Modeling for Distributionally Robust Offline Reinforcement Learning** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span>

_Johns Hopkins University — with Prof. Laixi Shi and collaborators_

A robust offline-RL framework that builds the uncertainty set from a **conditional flow model** instead of a rectangular, divergence-ball set: shared flow parameters couple shifts across state–action pairs, and the **flow-matching loss** serves as the discrepancy measure, which provably implies a Wasserstein-2 bound. The flow model is **adversarially fine-tuned** against the current policy with an inverse-propensity-weighted, PPO-style objective under the flow-matching constraint, and the generated adverse _H_-step trajectories become conservative critic targets for IQL, CQL or BCQ backbones. It achieves the best OOD score across six MuJoCo task–dataset settings, exceeding the strongest baseline by **6.7 normalized points**, with gains across all three backbones and on an EPANET water-distribution-network control case study.
<span style="color: var(--global-text-color-light)">_Under review._</span>

**Track-Any-Point Foundation Model for Endoscopic Scenes** &nbsp; <span style="color: var(--global-text-color-light)">· Feb 2026 – Present</span>

_ARCADE Lab, Johns Hopkins University — with Dr. Lalithkumar Seenivasan_

A track-any-point model for endoscopic and bronchoscopic navigation, where textureless anatomy, specular reflections, tissue deformation, occlusion and rapid camera motion break existing trackers. It extends AllTracker with a **dual-correlation** design that fuses long-range anchor correspondence with flow-aligned adjacent-frame matching (**91.9% δ<sub>avg</sub>**, above the anchor-only baseline), and a cosine-gated **feature memory** that cuts invisible-point loss by ~9% for recovery from occlusion and re-entry. Sliding-window inference with feature reuse runs in real time (~120–156 fps, ~0.4 GB memory).
<span style="color: var(--global-text-color-light)">_Manuscript in preparation._</span>

**Backdoor Attacks on Multivariate Time Series Forecasting with Missing Values** &nbsp; <span style="color: var(--global-text-color-light)">· Dec 2024 – May 2025</span>

_Undergraduate thesis, DBIS Lab, Nankai University — with Dr. Xiangrui Cai_

A backdoor-attack framework for multivariate forecasting under realistic missing-value scenarios, where prior attacks assume complete inputs: a critical-time-step-guided imputation strategy and dynamic trigger placement (missing-value density, prediction sensitivity, local volatility) balance effectiveness and stealth, giving **17–43%** relative improvement over baseline attack strategies on PeMS traffic datasets.
