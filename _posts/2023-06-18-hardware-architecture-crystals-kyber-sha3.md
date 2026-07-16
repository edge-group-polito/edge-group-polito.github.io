---
layout: post
title: "Hardware architecture for CRYSTALS-Kyber post-quantum cryptographic SHA-3 primitives"
date: 2023-06-18
authors: "Alessandra Dolmeta, Maurizio Martina, Guido Masera"
citation: "2023 18th Conference on Ph.D Research in Microelectronics and Electronics (PRIME), pp. 209-212, 2023"
paper_url: https://ieeexplore.ieee.org/abstract/document/10161780/
---

Once powerful enough quantum computers become feasible, many of the regularly used
cryptosystems will be completely useless. Thus, designing quantum-safe cryptosystems to
replace current algorithms is more crucial than ever. This paper presents the hardware
implementation of one of the fundamental building blocks of all post-quantum
cryptographic (PQC) algorithms, which are PQC-primitives, having NIST-PQC-finalists
CRYSTALS-Kyber algorithm as a target. This work analyzes Keccak sponge function and the
four SHA-3 algorithms used in CRYSTALS-Kyber, realizing the correct processing and
handling of input information and integrating the four standards into one implementation
for Kyber-III level of security. The synthesis results are provided for 65-nm technology,
while Artix7 XC7A75-3 is chosen as the implementation platform. The efficiency and the
performance of the proposed architecture are compared in terms of area, frequency, clock
cycles, and efficiency with the state-of-the-art.
