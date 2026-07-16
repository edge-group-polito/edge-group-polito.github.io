---
layout: post
title: "Stop Wasting your Cache! Bringing Machine Learning into Cache Computing"
date: 2025-05-28
authors: "Vincenzo Petrolo, Flavia Guella, Michele Caon, Guido Masera, Maurizio Martina"
citation: "CF '25 Companion: Proceedings of the 22nd ACM International Conference on Computing Frontiers: Workshops and Special Sessions, pp. 86-89, 2025"
paper_url: https://dl.acm.org/doi/abs/10.1145/3706594.3726983
---

The rapid evolution of Machine Learning (ML) workloads, particularly Deep Neural
Networks (DNNs) and Transformer-based models, has intensified demands on computing
architectures, highlighting the limitations of traditional von Neumann systems due to the
memory bottleneck. To address these challenges, this paper investigates the mapping of
fundamental Machine Learning (ML) operations onto ARCANE, a Near-Memory Computing
(NMC)-based architecture that integrates Vector Processing Units (VPUs) directly within
the data cache. ARCANE offers a flexible ISA-extension (xmnmc) abstracting memory
management, effectively reducing data movement and enhancing performance. We
specifically explore the acceleration capabilities of ARCANE when executing fundamental
Deep Neural Network (DNN) and Transformer-based operations. Experimental results show
that, with a contained area overhead, ARCANE achieves consistent speedups, delivering up
to 150× improvement in 2D convolution, 305× in Linear layer, and over 32× in Fused-Weight
Self-Attention (FWSA), compared to conventional CPU approaches. These findings underline
ARCANE's significant benefits in supporting efficient deployment of edge-oriented Machine
Learning (ML) workloads.
