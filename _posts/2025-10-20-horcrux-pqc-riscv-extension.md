---
layout: post
title: "HORCRUX - A Lightweight PQC-RISC-V eXtension Architecture"
date: 2025-10-20
authors: "Alessandra Dolmeta, Valeria Piscopo, Guido Masera, Maurizio Martina, Michael Hutter"
citation: "Cryptology ePrint Archive, Paper 2025/1934, 2025"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=8SRb1IsAAAAJ&citation_for_view=8SRb1IsAAAAJ:_FxGoFyzp5QC
repo_url: https://github.com/edge-group-polito/HORCRUX/tree/cup
---

This work presents a RISC-V extension for Post-Quantum Cryptography (PQC) called
HORCRUX, which provides a unified Instruction-Set Extension (ISE) supporting all
NIST-approved PQC algorithms. HORCRUX addresses the current fragmentation in hardware
support, where existing extensions typically focus on individual algorithms or limited
subsets of PQC schemes, and targets the common kernels shared across ML-KEM, ML-DSA,
SLH-DSA, and HQC. To address the primary computational bottlenecks of all these
algorithms (namely, modular arithmetic, matrix multiplication, and hash transformations),
the extension introduces new RISC-V instructions executed by a tightly coupled
coprocessor. This coprocessor requires only minimal hardware resources, making the
architecture efficient for constrained devices while still providing substantial
acceleration. An experimental evaluation on a Zynq UltraScale+ FPGA demonstrates speedups
of up to 3× for lattice and hash-based schemes, and over 30× for code-based schemes,
while adding less than 2,900 LUTs and 400 FFs to the design. The extension's modular
structure maintains backward compatibility with standard RISC-V cores, offering a
scalable solution for deploying PQC on highly constrained embedded systems.
