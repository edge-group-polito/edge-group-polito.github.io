---
layout: post
title: "Towards Achieving Vertical Reuse in SoC-Level Verification"
date: 2025-10-28
authors: "Petr Bardonek, Alessandra Dolmeta, Marcela Zachariášová, Guido Masera"
citation: "2025 IEEE Nordic Circuits and Systems Conference (NorCAS), pp. 1-7, 2025"
paper_url: https://scholar.google.com/citations?view_op=view_citation&hl=it&user=8SRb1IsAAAAJ&citation_for_view=8SRb1IsAAAAJ:Se3iqnhoufwC
repo_url: https://github.com/edge-group-polito/keccak_integration
---

Recent trends in AI-assisted design and new approaches to accelerate overall design
processes are contributing to the increasing complexity of System-on-Chip (SoC) designs.
Unfortunately, advancement in verification methods has not kept pace, leading to a
widening verification gap. This gap underscores the growing importance of reusing
verification components. Although reusing components at the testbench level is possible,
the portability of verification tests and scenarios in complex SoC integrations remains
inadequate and underexplored. The Portable Stimulus Standard (PSS) aims to enhance reuse
through a model-based approach, where Portable Models (PMs) capture the intent of
verification tests in a significantly more abstract manner. Although transitioning to
this higher level of abstraction is promising, it still entails a considerable manual
burden, even when utilizing PSS. PMs connect to the Design Under Verification (DUV) via
realization-layer bindings, which may vary as one moves from a module-level to a
SoC-level context. The authors propose an automation approach, represented in their
unique toolchain based on static analysis, that facilitates the binding of modular PMs to
a top-level PM. This paper demonstrates the application of this toolchain in a full SoC
integration context, using a Keccak cryptographic accelerator integrated through both
loosely coupled and tightly coupled architectures as the DUV. The study illustrates that
static analysis can support vertical reuse across multiple design hierarchy levels.
However, as integration reaches the SoC scale, it increasingly intersects with
software-driven control and structural encapsulation, necessitating additional modeling
efforts. These findings define the limitations of structural automation for vertical
reuse and outline directions for enhancing methodologies and tool support for SoC-scale
verification.
