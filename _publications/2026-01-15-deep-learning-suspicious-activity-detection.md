---
title: "Deep Learning Frameworks for Suspicious Activity Detection"
collection: publications
permalink: /publication/2026-01-15-academic-thesis
excerpt: "Undergraduate Academic Thesis at BRAC University benchmarking spatiotemporal architectures across 5 public surveillance benchmarks and proposing Nano3D with Grad-CAM visual interpretability."
date: 2026-01-15
category: thesis
venue: 'Department of Computer Science & Engineering, BRAC University'
paperurl: 'https://github.com/mohiuddin-khan-shiam/Nano3D'
citation: 'S. M. Mohiuddin Khan Shiam. (2026). "Deep Learning Frameworks for Suspicious Activity Detection." Academic Thesis, Department of Computer Science & Engineering, BRAC University. Supervised by Prof. Dr. Amitabha Chakrabarty & Prof. Dr. Md. Golam Rabiul Alam.'
---

<div class="pub-badges">
  <span class="badge badge--thesis"><i class="fa-solid fa-graduation-cap"></i> Academic Thesis (2026)</span>
  <span class="badge badge--bracu"><i class="fa-solid fa-building-columns"></i> BRAC University</span>
  <span class="badge badge--code"><i class="fab fa-github"></i> Code: Nano3D</span>
</div>

### Thesis Overview

**Supervisors**:  
- **Prof. Dr. Amitabha Chakrabarty**, Professor, Dept. of Computer Science & Engineering, BRAC University  
- **Prof. Dr. Md. Golam Rabiul Alam**, Professor, Dept. of Computer Science & Engineering, BRAC University  

Automated detection of violent altercations, theft, and erratic behaviors in public surveillance streams is vital for municipal safety and proactive threat mitigation. This thesis systematically investigates spatiotemporal deep learning paradigms, examining the architectural trade-offs between dense temporal modeling and edge compute constraints.

### Key Contributions & Results

1. **Rigorous Multi-Dataset Benchmarking**: Conducted comprehensive empirical evaluation of state-of-the-art spatiotemporal models under identical evaluation metrics across 5 public datasets: **UCF-Crime**, **XD-Violence**, **RWF-2000**, **UBI-Fights**, and **SCVD**.
2. **Nano3D Edge Architecture Formulation**: Designed and trained Nano3D, reaching **88.7% overall classification accuracy**, **0.947 Area Under Curve (AUC)**, and **7.19 ms inference latency** with only **486,000 parameters** (1.86 MB file footprint).
3. **Spatiotemporal Attribution via Grad-CAM**: Integrated gradient-weighted class activation mapping extended across temporal video slices, confirming that feature representations localize accurately onto actors and objects undergoing anomalous interaction.

[View Code & Benchmarks on GitHub](https://github.com/mohiuddin-khan-shiam/Nano3D){: .btn .btn--primary target="_blank" rel="noopener noreferrer"}
