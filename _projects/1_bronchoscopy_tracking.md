---
layout: page
title: Point Tracking for Bronchoscopy
description: Adjacent-frame correlation for robust point tracking in low-texture, high-glare airway video.
importance: 3
category: research
---

**ARCADE Lab, Johns Hopkins University · Feb 2026 – Present**

- Adapting an AllTracker-style point tracker to bronchoscopy, where textureless airway walls, illumination changes, and specular reflections break long-range query-anchored matching.
- Introducing an **adjacent-frame correlation** module that estimates frame-to-frame optical flow and chains it for robust long-horizon trajectory tracking.
- Pairing it with a **knowledge-distillation** scheme (Transformer teacher → lightweight CNN student with D2-Net-style features) targeting real-time deployment at **< 30 ms latency**.

_Manuscript in preparation._
