---
layout: post
title: "RISC-V Based Keccak Co-Processor for NIST Post-Quantum Cryptography Standards"
date: 2025-05-25
authors: "Alessandra Dolmeta, Valeria Piscopo, Mattia Mirigaldi, Maurizio Martina, Guido Masera"
citation: "2025 IEEE International Symposium on Circuits and Systems (ISCAS), pp. 1-5, 2025"
paper_url: https://ieeexplore.ieee.org/abstract/document/11043433
repo_url: https://github.com/edge-group-polito/KRONOS/tree/coproc
---

This paper presents the design and implementation of a RISC-V-based Keccak co-processor
optimized for Post-Quantum Cryptography (PQC) algorithms. Leveraging the Core-V eXtension
InterFace (CV-X-IF), the co-processor extends the Instruction Set Architecture (ISA) with
three custom instructions tailored for cryptographic operations. This allows seamless
integration into various PQC schemes, tested across the multiple standards proposed by
the National Institute of Standards and Technology (NIST), including CRYSTALS-Kyber,
CRYSTALS-Dilithium, SPHINCS+, and FALCON, which are designed to withstand quantum
attacks. By employing tightly coupled hardware acceleration, the Keccak co-processor
dramatically reduces the computational overhead of hash-based operations central to
these algorithms. The implementation is realized on a Xilinx Artix 7 FPGA, achieving a
clock cycles' improvement up to 75% and 19% resource overhead. The results presented
herein demonstrate significant performance enhancement over the state of the art,
underscoring its effectiveness for cryptographic applications.
