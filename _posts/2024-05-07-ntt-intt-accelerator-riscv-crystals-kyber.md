---
layout: post
title: "Implementation and integration of NTT/INTT accelerator on RISC-V for CRYSTALS-Kyber"
date: 2024-05-07
authors: "Alessandra Dolmeta, Emanuele Valpreda, Maurizio Martina, Guido Masera"
citation: "CF '24: Proceedings of the 21st ACM International Conference on Computing Frontiers: Workshops and Special Sessions, pp. 59-62, 2024"
paper_url: https://dl.acm.org/doi/abs/10.1145/3637543.3652872
repo_url: https://github.com/edge-group-polito/KALIPSO
---

This paper presents a comprehensive study on the implementation of a RISC-V-based
memory-mapped accelerator designed for Number Theoretic Transform (NTT) and Inverse
Number Theoretic Transform (INTT) operations within the context of the post-quantum
cryptographic algorithm CRYSTALS-Kyber. The primary focus lies in the performance
evaluation of the algorithm, with a particular emphasis on minimizing the overhead
associated with transferring data between the core and the implemented IP. The analysis
includes a deep dive into the intricacies of data transfer, leveraging Direct Memory
Access (DMA) to efficiently reduce overhead. The evaluation results show that our
approach, when applied to a X-HEEP core, achieves up to 15.7× and 19.6× improvement in
cycle count for NTT and INTT respectively, compared to the base software implementation.
To this end, we also demonstrate the efficacy of the proposed memory-mapped accelerator
in enhancing the overall performance of CRYSTALS-Kyber, thereby contributing to the
advancement of secure cryptographic systems in the post-quantum era.
