---
layout: post
title: "ARCANE: Adaptive RISC-V Cache Architecture for Near-memory Extensions"
date: 2025-06-22
authors: "Vincenzo Petrolo, Flavia Guella, Michele Caon, Pasquale Davide Schiavone, Guido Masera, Maurizio Martina"
citation: "2025 62nd ACM/IEEE Design Automation Conference (DAC), pp. 1-6, 2025"
paper_url: https://ieeexplore.ieee.org/abstract/document/11132598/
---

Modern data-driven applications expose limitations of von Neumann architectures —
extensive data movement, low throughput, and poor energy efficiency. Accelerators
improve performance but lack flexibility and require data transfers. Existing compute
in- and near-memory solutions mitigate these issues but face usability challenges due to
data placement constraints. We propose a novel cache architecture that doubles as a
tightly-coupled compute-near-memory coprocessor. Our RISC-V cache controller executes
custom instructions from the host CPU using vector operations dispatched to near-memory
vector processing units within the cache memory subsystem. This architecture abstracts
memory synchronization and data mapping from application software while offering
software-based Instruction Set Architecture extensibility. Our implementation shows 30×
to 84× performance improvement when operating on 8-bit data over the same system with a
traditional cache when executing a worst-case 32-bit CNN workload, with only 41.3% area
overhead.
