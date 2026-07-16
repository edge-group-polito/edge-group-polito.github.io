---
layout: post
title: "CHIMERA: Cryptographic Hardware for Integrated Multipurpose Engine on RISC-V with ASCON"
date: 2025-07-06
authors: "Alessandra Dolmeta, Valeria Piscopo, Maurizio Martina, Guido Masera"
citation: "2025 IEEE Computer Society Annual Symposium on VLSI (ISVLSI), pp. 1-6, 2025"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=8SRb1IsAAAAJ&citation_for_view=8SRb1IsAAAAJ:ufrVoPGSRksC
repo_url: https://github.com/edge-group-polito/CHIMERA
---

In the context of the growing Internet-of-Things (IoT) ecosystem, where security and
privacy concerns are critical due to the limited resources of connected devices,
lightweight cryptography plays a vital role. ASCON, a lightweight cryptographic algorithm
designed for constrained environments, offers robust security mechanisms such as
Authenticated Encryption with Associated Data (AEAD), hashing, Message Authentication
Code (MAC) generation and Pseudorandom Functions (PRF). In this work, we introduce
CHIMERA, an Application Specific Instruction Set Processor (ASIP) architecture tailored
to efficiently compute the ASCON algorithm on 32-bit RISC processors. The ASIP interfaces
with the RISC-V core via the Core-V eXtension Interface (CV-X-IF), a novel communication
mechanism. CHIMERA functions as a multipurpose coprocessor, supporting AEAD (ASCON-128,
ASCON-128a) and hashing (Hash, Hasha). We present two versions of CHIMERA: the Complete
Round (CR) version, a tightly coupled accelerator that delivers high performance at a
higher hardware cost, and the Bitwise Rotation Unit (BRU) version, an Instruction Set
Extension (ISE) offering lower efficiency but minimal area requirements. The design has
been implemented on both Zynq Ultrascale+ FPGA and ASIC platforms, with results comparing
the two versions and evaluating their performance relative to the state-of-the-art.
