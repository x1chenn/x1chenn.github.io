---
layout: page
title: Hybrid Defect Detection for Ceramic Tiles
description: Tiny-defect detection on ultra-high-resolution industrial images with an improved YOLOv8.
importance: 6
category: research
---

**Group Leader — Course Project, JHU 601.661 Computer Vision · Sep 2025 – Dec 2025**

- Sliced 8192×6000 industrial images via sliding windows into a ~19.5K-image localized dataset to mitigate small-object feature loss.
- Improved YOLOv8n with CBAM attention, SPD convolution, a custom Weighted CIoU-NWD loss, and a C2f-Faster (Partial Convolution) backbone.
- Achieved **+5.2% mAP → 71.2%** while maintaining **133 FPS** at only 3.10M parameters.
