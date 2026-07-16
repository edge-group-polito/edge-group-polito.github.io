---
layout: post
title: "ATHOS: A Hybrid Accelerator for PQC CRYSTALS-Algorithms Exploiting New CV-X-IF Interface"
date: 2024-12-04
authors: "Alessandra Dolmeta, Maurizio Martina, Guido Masera"
citation: "IEEE Access, vol. 12, pp. 182340-182352, 2024"
paper_url: https://ieeexplore.ieee.org/abstract/document/10776955
repo_url: https://github.com/edge-group-polito/ATHOS
---

ATHOS (Accelerated Technology for Hardware Optimization with RISC-V) is introduced as a
robust solution for enhancing cryptographic operations, explicitly designed for RISC-V
architectures. Addressing the challenges of implementing cryptographic algorithms, ATHOS
leverages a combination of both tightly and loosely coupled accelerators. A key innovation
of ATHOS is its exploitation of the CV32E40X core via the novel Core-V eXtension
InterFace (CV-X-IF). This pioneering work is one of the first to utilize this interface
in real-world applications, offering a unique foundation for extensive exploration of
acceleration approaches. Utilizing the CV-X-IF simplifies the insertion of new
instructions into the Instruction Set Architecture (ISA) and streamlines the integration
of tightly coupled accelerators without requiring modifications to the toolchain. This
work focuses on the implementation and integration of various accelerators into the
RISC-V microcontroller X-HEEP, adding new instructions and external IPs for the Numeric
Theoretic Transform (NTT), its Inverse (INTT), and Keccak transformation. Our complete
architecture is implemented on ASIC 65μm technology, resulting in a 1.47× area overhead
for the microcontroller. Additionally, it improves CRYSTALS-Kyber's and
CRYSTALS-Dilithium's total clock cycle respectively by up to 7.74× and to 4.12× compared
to the baseline software implementation, demonstrating the potential of this hybrid
system and marking one of the first real applications of the CV-X-IF interface.
