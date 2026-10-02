---
layout: about
title: about
permalink: /
subtitle: M.S.E. in Computer Science @ <a href='https://www.jhu.edu/'>Johns Hopkins University</a> | Robust RL · Robot Learning · Generative World Models

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

Hi! I'm **Xi Chen (陈希)**, a second-year **M.S.E. student in Computer Science** at **Johns Hopkins University**. I am fortunate to be advised by [Prof. Laixi Shi](https://laixishi.github.io/index.html)! I also work closely with Prof. Jianyi Yang on generative world models for robust offline RL, and with Dr. Lalithkumar Seenivasan in the ARCADE Lab on perception for surgical robots. Before JHU, I received my B.Eng. in Computer Science from **Nankai University**.

I want to build decision-making agents that keep working when deployment differs from training, and I am **applying for a Ph.D.** to pursue this direction. My research focuses on:

- 🛡️ **Robust reinforcement learning** — Algorithms and benchmarks for policies that survive deployment uncertainty: shifts in dynamics, observations, actions, rewards, control latency and scene semantics. I lead a unified library and benchmark that trains and evaluates robust online, offline and safe RL algorithms under one train–disrupt–evaluate protocol, so that each robustness mechanism can be matched to the channel it actually defends.
- 🤖 **Robot learning** — Carrying robust RL from standard control to real robotic stacks: humanoid locomotion and manipulation in Isaac Lab, frozen vision–language–action policies under sim-to-real shift, and reliable perception (point tracking) for surgical robots, where the perception backbone, the world model and the policy must hold up together.
- 🌍 **Generative world models for RL** — Flow-matching and diffusion models as trajectory-level world models: multi-step value expansion for offline RL without compounding one-step error, and generative uncertainty sets whose adversarial fine-tuning yields distributionally robust policies against diverse yet plausible dynamics shifts.

Earlier work spans time-series learning, generative modeling and computer vision. I enjoy problems where robust decision-making meets real deployment constraints.

---

## news

{% include news.liquid limit=true %}

## selected research projects

**A Unified Library and Benchmark for Robust Reinforcement Learning Algorithms** &nbsp; <span style="color: var(--global-text-color-light)">· 2026 – Present</span>

_Johns Hopkins University — with Prof. Laixi Shi and collaborators_

An algorithm-centric library and benchmark for robust RL under deployment uncertainty. It integrates **22 algorithms** (6 standard, 16 robust online, offline and safe), organizes them by mechanism and claimed uncertainty, and evaluates every frozen policy under one protocol on a **shift toolbox of six sources** (dynamics, observation, action, reward/cost, latency, semantic) with several modes and their compositions, across hundreds of perturbation configurations. The same interface runs on advanced robotic tasks — humanoid and manipulation in Isaac Lab and a frozen vision–language–action policy — to mimic the sim-to-real gap. The findings: robustness is channel-specific, and what a mechanism models is what it defends.
<span style="color: var(--global-text-color-light)">_Under review. Library and project website to be released after the review period._</span>

**Generative Uncertainty Modeling for Distributionally Robust Offline RL** &nbsp; <span style="color: var(--global-text-color-light)">· Apr 2026 – Present</span>

_Johns Hopkins University — with Prof. Laixi Shi, Prof. Jianyi Yang, and Jiaqi Wen_

A robust offline-RL framework that builds the uncertainty set from a **conditional flow model** instead of a rectangular, divergence-ball set: shared flow parameters couple shifts across state–action pairs, and the **flow-matching loss** serves as the discrepancy measure, which provably implies a Wasserstein-2 bound. The flow model is **adversarially fine-tuned** against the current policy with an inverse-propensity-weighted, PPO-style objective under the flow-matching constraint, and the generated adverse _H_-step trajectories become conservative critic targets for IQL, CQL or BCQ backbones. On MuJoCo dynamics shifts and an EPANET water-distribution-network control case study it improves OOD scores without sacrificing nominal performance.
<span style="color: var(--global-text-color-light)">_Under review._</span>

**Point Tracking for Bronchoscopy via Adjacent-Frame Correlation** &nbsp; <span style="color: var(--global-text-color-light)">· Feb 2026 – Present</span>

_ARCADE Lab, Johns Hopkins University — with Dr. Lalithkumar Seenivasan_

An AllTracker-style tracker adapted to bronchoscopy, where textureless airway walls, illumination shifts, and specular reflections break long-range query-anchored matching. An **adjacent-frame correlation** module estimates and chains frame-to-frame optical flow for robust tracking, distilled (Transformer teacher → lightweight CNN student with D2-Net-style features) for real-time deployment at **< 30 ms latency**.
<span style="color: var(--global-text-color-light)">_Manuscript in preparation._</span>

**Backdoor Attacks on Multivariate Time-Series Forecasting** &nbsp; <span style="color: var(--global-text-color-light)">· Dec 2024 – May 2025</span>

_Undergraduate thesis, DBIS Lab, Nankai University — with Dr. Xiangrui Cai_

A stealthy backdoor-attack framework for multivariate forecasting under realistic missing-value scenarios: invisible triggers at missing-value positions plus a critical-time-step imputation strategy preserve stealth while cutting attack MAE by **43%** versus baselines.
