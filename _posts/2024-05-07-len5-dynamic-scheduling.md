---
layout: post
title: "Seeing Beyond the Order: a LEN5 to Sharpen Edge Microprocessors with Dynamic Scheduling"
date: 2024-05-07
authors: "Michele Caon, Vincenzo Petrolo, Mattia Mirigaldi, Flavia Guella, Guido Masera, Maurizio Martina"
citation: "CF '24: Proceedings of the 21st ACM International Conference on Computing Frontiers: Workshops and Special Sessions, pp. 47-50, 2024"
paper_url: https://dl.acm.org/doi/abs/10.1145/3637543.3652880
---

In recent years, the shift towards data-driven workloads has underscored the limitations
of traditional Von Neumann embedded computers and centralized processing infrastructures.
Heterogeneous embedded Systems on Chip have emerged as a promising alternative offering
the performance and energy efficiency benefits of specialized accelerators alongside the
versatility of CPU-based systems. However, optimizing operation scheduling and resource
utilization at compile time remains a challenging task. In this context, modular
Instruction Set Architectures like RISC-V enable the development of tightly-coupled
coprocessors that share the code with the host CPU. Techniques exploiting
Instruction-Level Parallelism can mitigate the high latency of specialized hardware by
dynamically reordering and speculatively executing instructions. This paper presents the
first iteration of LEN5, a 64-bit RISC-V microprocessor featuring a modular, dynamically
scheduled execution pipeline with Out-of-Order execution and commit. Preliminary
implementation figures and benchmarking results over the Embench suite show significant
improvements in Instructions Per Cycle of more than 20% compared to simpler in-order
microarchitectures. Additionally, LEN5 achieves a 20% higher operating frequency when
integrated into a small, edge-oriented microcontroller. The 64-bit architecture also
enables up to a 2.4× reduction in the number of instructions required to execute
precision-sensitive workloads.
