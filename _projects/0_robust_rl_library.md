---
layout: page
title: Robust RL Library and Benchmark
description: A unified library and benchmark for robust reinforcement learning algorithms under deployment uncertainty.
importance: 1
category: research
---

**Johns Hopkins University — with Prof. Laixi Shi and collaborators · 2026 – Present**

- An **algorithm-centric library and benchmark** for robust RL: 22 algorithms (6 standard, 16 robust online, offline and safe), organized by robustness mechanism and the uncertainty each one claims to defend.
- A **shift toolbox of six sources** — dynamics, observation, action, reward/cost, latency and semantic — in five modes (parametric, stochastic, scheduled, adversarial, compound), declared as data and stacked on any environment without touching the algorithm.
- One **train–disrupt–evaluate protocol**: every frozen policy is scored on the same grid of hundreds of perturbation configurations, plus isolated and compound-shift studies, so a reported gain can be separated from the setup that produced it.
- The same interface instantiated on **advanced robotic tasks** — humanoid locomotion and drawer manipulation in Isaac Lab, and a frozen vision–language–action policy — to mimic the sim-to-real gap.
- Findings: robustness is **channel-specific**; what a mechanism models is what it defends, and claimed channels do not fully predict empirical strengths.

_Under review. Library and project website to be released after the review period._
