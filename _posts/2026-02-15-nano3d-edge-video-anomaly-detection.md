---
title: "Nano3D: Designing a 486K-Parameter 3D-CNN for Real-Time Edge Video Anomaly Detection"
date: 2026-02-15
permalink: /posts/2026/02/nano3d-edge-video-anomaly-detection/
tags:
  - Deep Learning
  - Computer Vision
  - Edge AI
  - Explainable AI
---

Automating surveillance video anomaly detection (VAD) is a crucial challenge for smart city infrastructure, transportation hubs, and public security. However, deploying state-of-the-art video anomaly detection systems in the real world presents a harsh trade-off: **model accuracy versus computational footprint**.

Standard spatiotemporal neural networks—such as **C3D**, **I3D**, and **3D ResNet-50**—contain between 25 million and 65 million parameters, requiring gigabytes of memory and dedicated server-class GPUs. When deployed on embedded edge devices like the NVIDIA Jetson Nano or low-power smart cameras, these heavy networks suffer from catastrophic frame drops, overheating, and excessive inference latency.

To address this challenge, in our recent work we designed **Nano3D**: an ultra-lightweight, explainable 3D Convolutional Neural Network containing only **486,000 parameters** with a disk footprint of **1.86 MB**, capable of real-time inference at **7.19 ms per clip** while achieving state-of-the-art accuracy across five benchmark surveillance datasets.

---

## The Architectural Design of Nano3D

Developing a spatiotemporal network that operates under 500K parameters requires rethinking how 3D convolutions capture spatial morphology and temporal motion simultaneously.

### 1. Factorized Spatiotemporal Convolutions $(2+1)\text{D}$
Full 3D convolutions ($k \times k \times k$) are computationally expensive because the number of multiplications scales with $k^3$. Nano3D decomposes full 3D convolutions into separate spatial and temporal operations:
- A spatial $1 \times 3 \times 3$ convolution capturing scene geometry, human poses, and object boundaries.
- Followed by a temporal $3 \times 1 \times 1$ convolution modeling velocity, trajectory changes, and sudden kinetic surges.

This factorization cuts the parameter footprint and FLOPs by over **65%** compared to full 3D kernels, while accelerating gradient backpropagation during training.

### 2. Depthwise Separable Bottlenecks
Within each residual stage, Nano3D employs depthwise separable 3D kernels followed by pointwise $1 \times 1 \times 1$ channel projections. By restricting the channel expansion ratio and placing Batch Normalization with Hard-Swish activations directly after the depthwise operation, the model retains non-linear expressive power while drastically cutting parameter redundancy.

### 3. Progressive Temporal Striding
Surveillance video contains high spatial and temporal redundancy across adjacent frames. Instead of processing raw 30 FPS streams naively, Nano3D utilizes non-uniform temporal striding:
- High temporal sampling rates during early feature extraction.
- Temporal pooling at deeper stages where semantic anomaly indicators (altercations, sudden falls, collisions) are consolidated.

---

## Empirical Benchmarks Across 5 Canonical Datasets

To ensure rigorous validation, Nano3D was benchmarked under uniform evaluation protocols against 5 widely studied surveillance datasets:
1. **UCF-Crime**: Large-scale real-world crime footage covering 13 anomaly categories.
2. **XD-Violence**: Multi-scene violent interaction sequences with audio-visual cues.
3. **RWF-2000**: Realistic surveillance fight detection benchmark.
4. **UBI-Fights**: Real-time physical altercation dataset with fine-grained annotations.
5. **SCVD (Smart City Video Dataset)**: Real-time public street surveillance anomalies.

### Results Summary

| Model Architecture | Parameters | Model Size | Inference Latency | Mean Accuracy | Mean AUC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **C3D Baseline** | 27.8M | 110.0 MB | 42.50 ms | 81.2% | 0.865 |
| **I3D (Two-Stream)** | 25.0M | 98.4 MB | 68.10 ms | 85.4% | 0.912 |
| **3D ResNet-50** | 46.2M | 185.0 MB | 54.30 ms | 86.1% | 0.924 |
| **Nano3D (Ours)** | **486K** | **1.86 MB** | **7.19 ms** | **88.7%** | **0.947** |

Despite having **less than 2% of the parameters** of 3D ResNet-50, Nano3D outperformed the baseline by **+2.6% in accuracy** and **+0.023 in AUC**, demonstrating that compact architectures with targeted inductive biases can match or exceed over-parameterized models on specialized video tasks.

---

## Explainability via Spatiotemporal Grad-CAM

A common drawback of automated surveillance AI is the "black-box" dilemma: when a system alerts security personnel to an anomaly, why was the alert triggered?

To ensure trustworthiness, Nano3D integrates **Spatiotemporal Gradient-Weighted Class Activation Mapping (Grad-CAM)**:

$$\alpha_k^c = \frac{1}{T \times H \times W} \sum_{t=1}^T \sum_{i=1}^H \sum_{j=1}^W \frac{\partial Y^c}{\partial A_{t, i, j}^k}$$

$$L_{\text{Grad-CAM}}^c = \text{ReLU}\left(\sum_k \alpha_k^c A^k\right)$$

Where $A^k$ represents the feature activation map of the final convolutional block across time dimension $T$ and spatial dimensions $H \times W$, and $Y^c$ is the score for anomaly class $c$.

By backpropagating the gradients of the anomaly logit to the final separable 3D convolution layer, Nano3D produces **spatiotemporal heatmaps** that illuminate exactly which actors and moving entities contributed to the anomaly detection score. This eliminates false alarms caused by moving foliage or ambient lighting shifts and allows human operators to verify alerts instantly.

---

## Edge Deployment & Next Steps

When compiled with **TensorRT** and evaluated on an **NVIDIA Jetson** embedded platform:
- Memory footprint during inference: **< 180 MB VRAM**.
- Throughput: **> 138 FPS** sustained.
- Thermal footprint: Minimal heat throttling under continuous 24-hour operation.

The full PyTorch code and model weights are available on GitHub: [mohiuddin-khan-shiam/Nano3D](https://github.com/mohiuddin-khan-shiam/Nano3D). We look forward to extending Nano3D with multimodal sensor integration and event-camera streams in upcoming research.
