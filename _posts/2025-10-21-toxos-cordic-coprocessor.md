---
layout: post
title: "TOXOS: Spinning Up Nonlinearity in On-Vehicle Inference with a RISC-V CORDIC Coprocessor"
date: 2025-10-21
authors: "Luigi Giuffrida, Guido Masera, Maurizio Martina"
citation: "Technologies, vol. 13, no. 10, article 479, 2025"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=pBBFNnwAAAAJ&citation_for_view=pBBFNnwAAAAJ:roLk4NBRz8UC
---

The rapid advancement of artificial intelligence in automotive applications,
particularly in Advanced Driver-Assistance Systems (ADAS) and smart battery management on
electric vehicles, increases the demand for efficient near-sensor processing. While the
problem of linear algebra in machine learning is well-addressed by existing accelerators,
the computation of nonlinear activation functions is usually delegated to the host CPU,
resulting in energy inefficiency and high computational costs. This paper introduces
TOXOS, a RISC-V-compliant coprocessor designed to address this challenge. TOXOS
implements the COordinate Rotation DIgital Computer (CORDIC) algorithm to efficiently
compute nonlinear functions. Taking advantage of RISC-V modularity and extendability,
TOXOS seamlessly integrates with existing computing architectures. The coprocessor's
configurability enables fine-tuning of the area-performance tradeoff by adjusting the
internal parallelism, the CORDIC iteration count, and the overall latency. Our
implementation on a 65nm technology demonstrates a significant improvement over
CPU-based solutions, showcasing a considerable speedup compared to the glibc
implementation of nonlinear functions. To validate TOXOS's real-world impact, we
integrated TOXOS in an actual RISC-V microcontroller targeting the on-vehicle execution
of machine learning models. This work addresses a critical gap in transcendental
function computation for AI, enabling real-time decision-making for autonomous driving
systems, maintaining the power efficiency crucial for electric vehicles.
