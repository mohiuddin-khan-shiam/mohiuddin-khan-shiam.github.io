---
title: "Nano3D: Explainable Ultra-Lightweight Deep Learning Model for Video Anomaly Detection"
excerpt: "Resource-efficient 3D-CNN architecture containing only 486K parameters (1.86 MB model size) achieving 88.7% accuracy and 7.19 ms latency on edge devices with spatiotemporal Grad-CAM attribution."
collection: portfolio
date: 2026-02-01
permalink: /portfolio/nano3d/
---

<div class="project-header-box">
  <span class="badge badge--tools"><i class="fa-solid fa-video"></i> Computer Vision & Edge AI</span>
  <span class="badge badge--tools"><i class="fa-solid fa-microchip"></i> 486K Params | 7.19 ms Latency</span>
  <span class="badge badge--code"><i class="fab fa-github"></i> <a href="https://github.com/mohiuddin-khan-shiam/Nano3D" target="_blank" rel="noopener noreferrer">GitHub: Nano3D</a></span>
</div>

### Project Overview

**Nano3D** is an ultra-compact 3D Convolutional Neural Network specifically designed for automated surveillance anomaly detection on resource-constrained edge computing platforms (such as NVIDIA Jetson and embedded IoT hardware).

While standard video anomaly detection frameworks rely on multi-million parameter networks requiring high-wattage server GPUs, Nano3D achieves state-of-the-art detection precision with an astonishingly small **1.86 MB** model footprint.

### Benchmark Highlights

- **Parameter Count**: Only **486,000 parameters** (~95% fewer than standard 3D Conv baselines).
- **Latency & Throughput**: **7.19 ms** per clip inference latency, operating at real-time speeds (>130 FPS).
- **Cross-Dataset Performance**: Benchmarked across **UCF-Crime**, **XD-Violence**, **RWF-2000**, **UBI-Fights**, and **SCVD**, delivering **88.7% accuracy** and **0.947 AUC**.
- **Spatiotemporal Grad-CAM**: Integrated visual explanations showing dynamic heatmaps where violent altercations, fights, or anomalous behaviors are localized in time and space.

[Explore Nano3D on GitHub](https://github.com/mohiuddin-khan-shiam/Nano3D){: .btn .btn--primary target="_blank" rel="noopener noreferrer"}
