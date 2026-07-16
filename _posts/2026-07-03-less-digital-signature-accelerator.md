---
layout: post
title: "A Lightweight Accelerator for the LESS Digital Signature Scheme"
date: 2026-07-03
authors: "Giuseppe Cutrera, Alessandra Dolmeta, Valeria Piscopo, Maurizio Martina, Guido Masera"
citation: "Cryptography, vol. 10, no. 4, article 45, 2026"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=8SRb1IsAAAAJ&citation_for_view=8SRb1IsAAAAJ:hqOjcs7Dif8C
---

The Linear Equivalence Signature Scheme (LESS) is a code-based post-quantum candidate in
the National Institute of Standards and Technology's (NIST) standardization process for
additional digital signatures. In this paper, we present an area-efficient FPGA
accelerator for the Reduced Row Echelon Form (RREF) kernel of LESS, designed for embedded
RISC-V SoCs where resource overhead is the primary constraint. Our architecture targets
the scheme's primary computational bottleneck: the linear-algebra core responsible for
RREF processing. By implementing an optimized pivot-reuse workflow, our design
significantly reduces redundant row-reduction operations across related computations.
The accelerator features a matrix-oriented execution engine paired with a streaming
control interface to minimize synchronization overhead. Implementation on a Xilinx
Artix-7 FPGA shows that despite its compact footprint, the accelerator achieves up to 21×
speedup over the embedded software RREF baseline. By prioritizing a minimalist footprint,
our design requires only 1.38 to 8.7 KeSlice, depending on the targeted security level. By
covering all LESS security levels and providing comparisons with existing post-quantum
cryptographic hardware, this work establishes a performance baseline for a signature
scheme that has remained largely unexplored in the hardware domain.
