---
layout: post
title: "A High-Entropy True Random Number Generator with Keccak Conditioning for FPGA"
date: 2025-03-08
authors: "Valeria Piscopo, Alessandra Dolmeta, Mattia Mirigaldi, Maurizio Martina, Guido Masera"
citation: "Sensors, vol. 25, no. 6, article 1678, 2025"
paper_url: https://www.mdpi.com/1424-8220/25/6/1678
---

Any cryptographic system strongly relies on randomness to ensure robust encryption and
masking methods. True Random Number Generators play a fundamental role in this context.
The National Institute of Standards and Technology (NIST) and the Bundesamt für
Sicherheit in der Informationstechnik (BSI) provide guidelines for designing reliable
entropy sources to fuel cryptographic Random Bit Generators. This work presents a highly
parameterized, open-source implementation of a TRNG based on ring oscillators,
complemented by an optimized Keccak conditioning unit. The design process is accompanied
by a thorough study of the relevant literature and standards, specifying the requirements
for reliable entropy sources in cryptographic systems. The design of the TRNG proposed in
this paper aims to strike a balance between area, throughput, power consumption, and
entropy, while adhering to these guidelines. The proposed design has undergone extensive
testing and validation and has successfully passed the NIST SP 800-22, NIST SP 800-90B,
and BSI AIS-31 tests, achieving a min-entropy per bit of 0.9982 (NIST) and 0.9998 (BSI).
