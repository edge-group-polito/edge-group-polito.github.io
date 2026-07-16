---
layout: post
title: "Just TestIt! An SBST Approach To Automate System-Integration Testing"
date: 2025-05-28
authors: "Tommaso Terzano, Luigi Giuffrida, Juan Sapriza, Pasquale Davide Schiavone, Guido Masera, David Atienza, Luciano Lavagno, Maurizio Martina"
citation: "CF '25 Companion: Proceedings of the 22nd ACM International Conference on Computing Frontiers: Workshops and Special Sessions, pp. 74-77, 2025"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=pBBFNnwAAAAJ&citation_for_view=pBBFNnwAAAAJ:LkGwnXOMwfcC
---

This paper introduces TestIt, an open-source Python package designed to automate
full-system integration testing using a Software-Based Self-Test (SBST) approach. By
dynamically generating test vectors and golden references, TestIt significantly reduces
development time and complexity while supporting both simulation and FPGA environments.
Its flexible design positions TestIt as a key enabler for the widespread adoption of
CI/CD methodologies in open-source RTL development. A case study on the X-HEEP RISC-V
microcontroller (MCU), which integrates a custom accelerator, showcases TestIt's ability
to detect hardware and software faults that traditional formal methods may overlook.
Furthermore, the case study highlights how TestIt can be leveraged to characterize system
performance with minimal effort. By automating testing on the PYNQ-Z2 FPGA development
board, we achieved a 11× speed-up with respect to RTL simulations.
