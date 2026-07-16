---
layout: post
title: "Implementation and integration of Keccak accelerator on RISC-V for CRYSTALS-Kyber"
date: 2023-05-09
authors: "Alessandra Dolmeta, Mattia Mirigaldi, Maurizio Martina, Guido Masera"
citation: "CF '23: Proceedings of the 20th ACM International Conference on Computing Frontiers, 2023, pp. 381–382"
paper_url: https://dl.acm.org/doi/abs/10.1145/3587135.3591432
repo_url: https://github.com/edge-group-polito/keccak_integration
---

One of the key metrics used for defying the security of the Internet of Things (IoT) is
data integrity, which mostly relies on the use of cryptographic hash functions. In the
last years, the National Institute of Standards and Technology (NIST) announced SHA-3 as
the new standard for better security. SHA-3 is also exploited in most of the current
post-quantum cryptographic (PQC) protocols. Nevertheless, the used algorithm, i.e. Keccak,
is computationally heavy and consequently limits its utilization in RISC-V-based Systems
on Chip (SoC). In this work, a Keccak accelerator is proposed to speed up SHA3
computations for the CRYSTALS-Kyber algorithm on the RISCV-based advanced microcontroller
PULPissimo. Compared to the plain SW implementation on RISC-V, our results show a speedup
factor of up to 2.79 at the expense of a 12.4% resources overhead.
