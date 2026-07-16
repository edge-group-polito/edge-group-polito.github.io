---
layout: post
title: "Scalability analysis of multi-bank near-memory computing in low-power SoCs"
date: 2025-10-12
authors: "Luigi Giuffrida, Pasquale Davide Schiavone, Michele Caon, Guido Masera, Maurizio Martina, David Atienza"
citation: "2025 IFIP/IEEE 33rd International Conference on Very Large Scale Integration (VLSI-SoC), pp. 1-4, 2025"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=pBBFNnwAAAAJ&citation_for_view=pBBFNnwAAAAJ:Se3iqnhoufwC
---

Machine learning and artificial intelligence are moving towards the edge, where the need
for high throughput with a constrained energy budget is more urgent than ever. During the
last few years, near-memory computing has emerged as a promising solution to address the
memory bandwidth and energy efficiency limitations of conventional von Neumann systems.
The recently proposed NM-Carus architecture combines vector-oriented computing
capabilities within a RISC-V programmable, configurable, and autonomous memory macro,
addressing the usability of near-memory computing from a software deployment standpoint.
In this paper, we explore the scalability of NM-Carus in terms of computation
parallelism, memory size and energy consumption. As a benchmarking platform, we rely on a
low-power microcontroller that features multiple instances of NM-Carus that target the
execution of biomedical applications. This exploration was performed on 16 nm TSMC
NM-Carus implementation, and we highlighted the benefits of technology scaling for a
previous implementation on 65 nm with respect to the overhead of replacing conventional
on-chip data SRAMs with near-memory computing banks. Overall, the paper presents a solid
baseline regarding the trade-offs in terms of area, performance, and energy efficiency of
integrating programmable near-memory computing in an existing edge-oriented system on
chip towards efficient edge AI architectures at the system level.
