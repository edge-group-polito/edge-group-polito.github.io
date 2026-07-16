---
layout: post
title: "Power Side-Channel Vulnerabilities of a RISC-V Cryptography Accelerator Integrated into CVA6 via Core-V eXtension Interface (CV-X-IF)"
date: 2025-09-20
authors: "Behnam Farnaghinejad, Davide Bellizia, Alessandra Dolmeta, Guido Masera, Antonio Porsia, Annachiara Ruospo, Stefano Di Carlo, Alessandro Savino, Ernesto Sanchez"
citation: "2025 IEEE International Test Conference (ITC), pp. 233-242, 2025"
paper_url: https://ieeexplore.ieee.org/abstract/document/11219849/
---

Modern RISC-V designs are increasingly integrating cryptographic accelerators to provide
better security features while enhancing performance; however, their vulnerability to
power side-channel attacks remains insufficiently investigated. This paper presents a
comprehensive evaluation of such vulnerabilities in a RISCV-based AES accelerator
connected via the Core-V eXtension Interface (CV-X-IF). The analysis begins at the RTL
using simulated power traces, employing KL (Kullback–Leibler) divergence alongside
established statistical attacks such as Correlation Power Analysis (CPA) and Differential
Power Analysis (DPA). Although the former serves as an early indicator of potential
leakage, simulation results highlight its limitations compared to CPA and DPA. To
validate these findings, leakage trends are further examined through FPGA-based power
measurement. The proposed methodology is designed to be broadly applicable to a range of
cryptographic workloads and accelerator architectures. It is demonstrated on an AES
accelerator implementing the scalar cryptographic extension (Zk) with pre-expanded keys.
Our findings reveal that side-channel vulnerabilities can persist even in tightly
integrated instruction pipelines, underscoring the importance of early-stage leakage
assessment. Notably, the close alignment between RTL-level simulations and FPGA-based
measurements highlights the effectiveness of the approach and its practical value for
guiding secure hardware design in RISC-V ecosystems. In particular, AES serves only as a
case of study; the proposed RTL and FPGA validation flow is generic and can be applied to
any cryptographic accelerator.
