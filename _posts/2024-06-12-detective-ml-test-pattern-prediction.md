---
layout: post
title: "DETECTive: Machine Learning-driven Automatic Test Pattern Prediction for Faults in Digital Circuits"
date: 2024-06-12
authors: "Vincenzo Petrolo, Sourav Medya, Mariagrazia Graziano, Debjit Pal"
citation: "GLSVLSI '24: Proceedings of the Great Lakes Symposium on VLSI 2024, pp. 32-37, 2024"
paper_url: https://dl.acm.org/doi/abs/10.1145/3649476.3658696
---

Due to the continuous technology scaling and the ever-increasing complexity and size of
the hardware designs, manufacturing defects have become a key obstacle in meeting
end-user demand. Despite decades of research, traditional test-generation techniques
often struggle to scale to massive and complex designs. Such scalability issues stem from
the numerous backtracking the traditional test generation techniques perform before
converging to a test pattern. In this work, we present DETECTive that leverages deep
learning on graphs to learn fault characteristics and predict test pattern(s) to expose
faults without requiring backtracking. DETECTive is trained on small circuits, and its
learned knowledge is transferable to predict test patterns for circuits that contain up
to 29× more gates than the training circuits. Since DETECTive avoids backtracking
completely, it can predict test patterns up to 15× faster than academic tools and up to
2× faster than commercial tools. DETECTive achieves up to 100% pattern accuracy on
synthetic designs and up to 95% test pattern accuracy on realistic designs. To our
knowledge, DETECTive is the first to leverage deep learning to predict test patterns for
digital hardware designs that can complement the traditional test generation techniques
for faster design closure.
