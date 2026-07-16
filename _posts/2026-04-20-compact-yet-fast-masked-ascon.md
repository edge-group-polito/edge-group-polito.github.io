---
layout: post
title: "Compact Yet Fast: An Efficient d-Order Masked Implementation of Ascon"
date: 2026-04-20
authors: "Mattia Mirigaldi, Nico Paninforni, Maurizio Martina, Guido Masera"
citation: "2026 Design, Automation & Test in Europe Conference (DATE), pp. 1-7, 2026"
paper_url: https://ieeexplore.ieee.org/abstract/document/11539534/
repo_url: https://github.com/edge-group-polito/compact-yet-fast-ascon
---

In this work, we present a generic side-channel protected design of Ascon that achieves
high efficiency by dynamically reconfiguring the hardware countermeasures during message
processing. The resultant implementation is protected and capable of meeting stringent
performance requirements whilst minimising resource overhead. The experimental results
obtained demonstrate that the implementation meets the required security and achieves
superior throughput-to-area ratio across all protection orders. Ascon, recently selected
by NIST as the lightweight cryptography standard, is widely deployed in
resource-constrained devices that demand both high performance and resistance against
threats such as side-channel analysis (SCA). Exploiting Ascon's mode-level structure,
which does not require protection against differential power analysis during bulk
operations, we introduce a modified masking gadget with dual functionality: serving as a
countermeasure during critical operations, and processing multiple data paths in parallel
to accelerate bulk computation. Our architecture supports any configurable security order
and instantiates only the minimum hardware resources needed to maximize throughput per
round. We also evaluate an enhanced Ascon architecture based on the Changing of the
Guards technique, which eliminates the need for fresh randomness. Security validation is
performed using fixed-vs-random t-tests on both first- and second-order masked
implementations. Finally, we compare our masked design against state-of-the-art
solutions.
