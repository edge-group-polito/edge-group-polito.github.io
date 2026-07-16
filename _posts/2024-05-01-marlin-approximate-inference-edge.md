---
layout: post
title: "MARLIN: A Co-Design Methodology for Approximate ReconfigurabLe Inference of Neural Networks at the Edge"
date: 2024-05-01
authors: "Flavia Guella, Emanuele Valpreda, Michele Caon, Guido Masera, Maurizio Martina"
citation: "IEEE Transactions on Circuits and Systems I: Regular Papers, vol. 71, no. 5, pp. 2105-2118, 2024"
paper_url: https://ieeexplore.ieee.org/abstract/document/10449675/
repo_url: https://github.com/edge-group-polito/MARLIN
---

The optimization of neural networks (NNs) is necessary to enable their deployment on
energy-constrained devices. State-of-the-art methods leverage approximate multipliers to
execute NNs reducing the inference energy without heavily affecting the accuracy.
However, previous works usually require a specialized hardware accelerator and are
limited to fixed multipliers or reconfigurable ones with few approximation levels. This
paper introduces MARLIN, a framework to deploy layerwise approximate NNs on PULP, a
microcontroller with a RISC-V core. A multiplier architecture, with runtime selection of
256 approximation levels, is developed and integrated into the PULP cluster cores,
enabling runtime configuration through control status register (CSR) instructions
embedded within the code. The PULP toolchain is adapted to incorporate the approximation
level selection within the instruction flow seamlessly. MARLIN leverages the genetic
algorithm NSGA-II to search for the best configurations among thousands of approximate
NNs. The framework is validated by simulating an approximate NN trained with the MNIST
dataset on PULP. Moreover, MARLIN is used to optimize and approximate six ResNet models
trained with the CIFAR-10 dataset. In particular, for ResNet-56, the most complex NN used
in the experiments, the multiplication energy is reduced by 23.9% while retaining 99% of
the accuracy of the exact model.
