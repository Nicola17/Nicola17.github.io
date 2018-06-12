---
layout: default
title: Nicola Pezzotti
---

About me
=======================

I'm a PhD candidate in the [Computer Graphics & Visualization](https://graphics.tudelft.nl/) group at the Delft University of Technology.
I'm supervised by [Prof. Anna Vilanova](https://graphics.tudelft.nl/anna-vilanova/), my Promotor (doctoral advisor) is [Prof. Elmar Eisemann](http://graphics.tudelft.nl/~eisemann/) and [Prof. Boudewijn P.F. Lelieveldt](https://www.lumc.nl/org/radiologie/medewerkers/1008040000252222) is my co-Promotor.
My research interest is mainly oriented towards the application of Machine Learning algorithms, in particular Manifold Learning and Deep Learning, in a Visual Analytics context.
I'm also interest in 3D Scanning Technologies and Geometry Processing.

I'm familiar with different programming languages and technologies. I generally work in C++/CUDA for performance reasons, however I'm also familiar with [Open|Web]GL, Python, TypeScript, JavaScript and Matlab.
I strongly believe that high-quality code is of main importance also in academia.

Projects
================

High-Dimensional Inspector
----
[Comment]: <>(![High-Dimensional Inspector Logo](/images/hdi_logo.png))

C++ library for scalable and interactive high-dimensional data analysis.
The core feature of [HDI](https://github.com/Nicola17/High-Dimensional-Inspector) is the implementation of the [Approximated-tSNE](http://nicola17.github.io/publications/2016_AtSNE.pdf) and [Hierarchical-SNE](http://nicola17.github.io/publications/2016_hsne/preprint.pdf), which together allow the visual analysis of millions of high-dimensional data points on a desktop computer.
The library also includes several visualizations, analytical workflows and data analysis algorithms.

TensorFlow.js tSNE
----
[Comment]: <>(![TensorFlow.js Logo](/images/tfjs_logo.png))

[tfjs-tsne](https://github.com/tensorflow/tfjs-tsne) is a module of the [TensorFlow.js](https://js.tensorflow.org/) library that implements the tSNE algorithm.
tfjs-tsne makes use of a [WebGL trick](https://arxiv.org/abs/1805.10817) to accelerate the gradient computation and the can be run in the client side of the web browser. Check out the [demo](https://nicola17.github.io/tfjs-tsne-demo/) on the MNIST dataset. This project featured on the [Google AI Blog](https://ai.googleblog.com/2018/06/realtime-tsne-visualizations-with.html).

Cytosplore
----
[Comment]: <>(![Cytosplore Logo](/images/cytosplore_logo.png))

[Cytosplore](https://www.cytosplore.org/) is an interactive visual analysis system for understanding how the immune system works. The goal of the analysis framework is to provide a clear picture of the immune systems cellular composition and the cells’ corresponding properties and functionality.


Selected Publications
================
A detailed list of my publications can be found at [this page](publications/)

* N. Pezzotti, A. Mordvintsev, T. Höllt, B.P.F. Lelieveldt, E. Eisemann, A. Vilanova. **Linear tSNE Optimization for the Web**. Transaction on Visualization and Computer Graphics (Proceedings of IEEE VIS 2017), 2018. [Preprint](https://arxiv.org/abs/1805.10817)
* V. van Unen\*, T. Hollt\*, N. Pezzotti\*, N. Li, M. J.T. Reinders, E. Eisemann, A. Vilanova, F. Koning, B. P.F. Lelieveldt. **Interactive Visual Analysis of Mass Cytometry Data by Hierarchical Stochastic Neighbor Embedding Reveals Rare Cell Types**. Nature Communications, 2017. [Website](https://www.nature.com/articles/s41467-017-01689-9) [PDF](https://www.nature.com/articles/s41467-017-01689-9.pdf)
* N. Pezzotti, T. Höllt, J. van Gemert, B.P.F. Lelieveldt, E. Eisemann, A. Vilanova. **DeepEyes: Progressive Visual Analytics for Designing Deep Neural Networks**. Transaction on Visualization and Computer Graphics (Proceedings of IEEE VIS 2017), 2018. [PDF](https://graphics.tudelft.nl/Publications-new/2018/PHVLEV18/paper216.pdf), [Video](https://graphics.tudelft.nl/Publications-new/2018/PHVLEV18/file216.avi)
* N. Pezzotti, T. Höllt, B.P.F. Lelieveldt, E. Eisemann, A. Vilanova. **Hierarchical Stochastic Neighbor Embedding**. Computer Graphics Forum (Proc. of EuroVis), 2016. [PDF](publications/2016_hsne/preprint.pdf), [Suppl. Mat.](publications/2016_hsne/experiments.pdf), [Video](publications/2016_hsne/sun_analysis.mp4), [Slides](http://www.slideshare.net/NicolaPezzotti/hierarchical-stochastic-neighbor-embedding)
* T. Höllt, N. Pezzotti, V. van Unen, F. Koning, E. Eisemann, B.P.F. Lelieveldt, A. Vilanova. **Cytosplore: Interactive Immune Cell Phenotyping for Large Single-Cell Datasets**. Computer Graphics Forum (Proc. of EuroVis), 2016. [PDF](https://graphics.tudelft.nl/Publications-new/2016/HPVKELV16/eurovis16_Cytosplore_Interactive_Immune_Cell_Phenotyping_for_Large_Single-Cell_Datasets.pdf)
* N. Pezzotti, B.P.F. Lelieveldt, L. van der Maaten, T. Höllt, E. Eisemann, and A. Vilanova. **Approximated and User Steerable tSNE for Progressive Visual Analytics**. Transaction on Visualization and Computer Graphics (Presented at IEEE VIS 2016), 2016. [PDF](publications/2016_AtSNE.pdf), [Suppl. Mat.](https://www.researchgate.net/publication/303305902_A-tSNE_supplemental_materials), [Video I](https://www.researchgate.net/publication/303305958_A-tSNE_Comparison_on_the_MNIST_dataset), [Video II](https://www.researchgate.net/publication/303305906_A-tSNE_Case_Study_I_-_Mouse_Brain), [Video III](https://www.researchgate.net/publication/303305908_A-tSNE_Case_Study_II_-_Data_Stream)

Awards
================
* **2006** - Awarded in "Expo Del capitale umano 2006" for academic merit
* **2005** - [Silver medal](https://www.olimpiadi-informatica.it/index.php/olimpiadi-italiane-2005.html) in the Italian selection for the *International Olympiad in Informatics* (IOI)
