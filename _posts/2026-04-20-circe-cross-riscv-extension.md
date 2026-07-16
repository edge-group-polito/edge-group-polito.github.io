---
layout: post
title: "CIRCE CROSS Integrated RISC-V Cryptographic Extension"
date: 2026-04-20
authors: "Alessandra Dolmeta, Valeria Piscopo, Maurizio Martina, Guido Masera"
citation: "2026 Design, Automation & Test in Europe Conference (DATE), pp. 1-3, 2026"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=8SRb1IsAAAAJ&citation_for_view=8SRb1IsAAAAJ:UebtZRa9Y70C
repo_url: https://github.com/edge-group-polito/CIRCE
---

Post-Quantum Cryptography (PQC) is moving from algorithm selection to deployment, where
performance, energy, and software portability are key constraints, especially on embedded
and IoT-class processors. Many PQC schemes stress general-purpose cores with irregular
control flow, large arithmetic workloads, and heavy memory traffic. Instruction-set
extensions (ISE) and tightly integrated accelerators offer a practical middle ground:
they speed up dominant kernels while preserving programmability and avoiding the rigidity
of fully fixed-function hardware. In this context, we target post-quantum digital
signatures, which remain under active evaluation, including NIST's 2023 call for
additional schemes. We focus on CROSS, a code-based signature built from zero-knowledge
proofs and the Restricted Syndrome Decoding Problem, and present CIRCE: a
RISC-V–integrated extension connected through the Core-V eXtension Interface (CV-X-IF).
CIRCE supports both R-SDP and R-SDP(G), runs across all official parameter sets without
hardware retuning, and achieves an average 2× speed-up on a Zynq UltraScale+ FPGA with an
ultra-compact footprint (down to 800 LUTs / 100 FFs).
