---
layout: post
title: "TYRCA: A RISC-V Tightly-Coupled Accelerator for Code-Based Cryptography"
date: 2025-03-31
authors: "Alessandra Dolmeta, Stefano Di Matteo, Emanuele Valea, Mikael Carmona, Antoine Loiseau, Maurizio Martina, Guido Masera"
citation: "2025 Design, Automation & Test in Europe Conference (DATE), pp. 1-7, 2025"
paper_url: https://ieeexplore.ieee.org/abstract/document/10993202/
---

Post-quantum cryptography (PQC) has garnered significant attention across various
communities, particularly with the National Institute of Standards and Technology (NIST)
advancing to the fourth round of PQC standardization. One of the leading candidates is
Hamming Quasi-Cyclic (HQC), which received a significant update on February 23, 2024.
This update, which introduces a classical dense-dense multiplication approach, has no
known dedicated hardware implementations yet. The innovative Core-V eXtension InterFace
(CV-X-IF) is a communication interface for RISC-V processors that significantly
facilitates the integration of new instructions to the Instruction Set Architecture
(ISA), through tightly connected accelerators. In this paper, we present a
TightlY-coupled accelerator for RISC-V for Code-based cryptogrAphy (TYRCA), proposing the
first fully tightly-coupled hardware implementation of the HQC-PQC algorithm, leveraging
the CV-X-IF. The proposed architecture is implemented on the Xilinx Kintex-7 FPGA.
Experimental results demonstrate that TYRCA reduces the execution time by 94% to 96% for
HQC-128, HQC-192, and HQC-256, showcasing its potential for efficient HQC code-based
cryptography.
