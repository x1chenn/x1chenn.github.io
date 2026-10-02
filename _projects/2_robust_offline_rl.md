---
layout: page
title: Generative Uncertainty Modeling for Robust Offline RL
description: Flow-based generative uncertainty sets, adversarially fine-tuned, for distributionally robust offline RL.
importance: 2
category: research
---

**Johns Hopkins University — with Prof. Laixi Shi and collaborators · Apr 2026 – Present**

- Replaces rectangular, divergence-ball uncertainty sets with a **generative uncertainty set** defined in the parameter space of a conditional flow model, so that shared parameters couple dynamics shifts across state–action pairs (non-rectangular, diverse yet plausible shifts).
- The **flow-matching loss** is the discrepancy measure: simulation-free and cheap to optimize, and it provably implies a Wasserstein-2 bound on the induced trajectory distribution.
- The flow model is **adversarially fine-tuned** against the current policy with an inverse-propensity-weighted relative-value objective in PPO style, under a Lagrangian flow-matching constraint; the generated adverse _H_-step trajectories serve as conservative critic targets for **IQL, CQL or BCQ** backbones.
- Improves OOD normalized scores on MuJoCo morphology, friction and gravity shifts over standard, robust and generative-model baselines without lowering nominal performance, and transfers to an **EPANET water-distribution-network** control case study.

_Under review._
