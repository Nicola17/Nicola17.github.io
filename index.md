---
layout: default
title: Nicola Pezzotti
---

About me
=======================

I'm a PhD student in the [Computer Graphics & Visulization](https://graphics.tudelft.nl/) group at the Delft University of Technology.
I'm supervised by [Prof. Anna Vilanova](https://graphics.tudelft.nl/anna-vilanova/), my promotor (doctoral advisor) is [Prof. Elmar Eisemann](http://graphics.tudelft.nl/~eisemann/) and [Prof. Boudewijn P.F. Lelieveldt](https://www.lumc.nl/org/radiologie/medewerkers/1008040000252222) is my co-promotor.
My research interest is mainly oriented towards the application of Machine Learning algorithms, in particular Manifold Learning and Deep Learning, in a Visual Analytics context.
I'm also interest in 3D Scanning Technologies and Computational Geometry.

I'm familiar with different programming languages and technologies. I generally work in C++/CUDA for performance reasons, however I'm also familiar with Python, JavaScript and Matlab. 
I strongly believe that high-quality code is of main importance also in academia.


Publications
================
A detailed list of my publications can be found at [this page](publications/)


* N. Pezzotti, T. Höllt, B.P.F. Lelieveldt, E. Eisemann, A. Vilanova. **Hierarchical Stochastic Neighbor Embedding**. Computer Graphics Forum (Proc. of EuroVis), 2016. [PDF](publications/2016_hsne/preprint.pdf), [Suppl. Mat.](publications/2016_hsne/experiments.pdf), [Video](publications/2016_hsne/sun_analysis.mp4)
* T. Höllt, N. Pezzotti, V. van Unen, F. Koning, E. Eisemann, B.P.F. Lelieveldt, A. Vilanova. **Cytosplore: Interactive Immune Cell Phenotyping for Large Single-Cell Datasets**. Computer Graphics Forum (Proc. of EuroVis), 2016. [PDF](https://graphics.tudelft.nl/Publications-new/2016/HPVKELV16/eurovis16_Cytosplore_Interactive_Immune_Cell_Phenotyping_for_Large_Single-Cell_Datasets.pdf)
* N. Pezzotti, B.P.F. Lelieveldt, L. van der Maaten, T. Höllt, E. Eisemann, and A. Vilanova. **Approximated and User Steerable tSNE for Progressive Visual Analytics**. *Transaction on Visualization and Computer Graphics (Presented at IEEE VIS 2016)*, 2016. [PDF](publications/2016_AtSNE.pdf), [Suppl. Mat.](https://www.researchgate.net/publication/303305902_A-tSNE_supplemental_materials), [Video I](https://www.researchgate.net/publication/303305958_A-tSNE_Comparison_on_the_MNIST_dataset), [Video II](https://www.researchgate.net/publication/303305906_A-tSNE_Case_Study_I_-_Mouse_Brain), [Video III](https://www.researchgate.net/publication/303305908_A-tSNE_Case_Study_II_-_Data_Stream)
* M. Centin, N. Pezzotti, A. Signoroni. **Poisson-driven seamless completion of triangular meshes**. *Computer Aided Geometric Design*, 2015. [PDF](publications/2014_Poisson_Driven_Seamless_completion.pdf), [Slides](2014_Poisson_Driven_Seamless_completion_presentation.pdf), [Bibtex](https://scholar.google.nl/scholar.bib?q=info:kmdSnlU02MkJ:scholar.google.com/&output=citation&scisig=AAGBfm0AAAAAVsRRbkgD9w_9f0NRdQmQFC2dA0Z5RWSy&scisf=4&hl=it&scfhb=1)
* F. Bonarrigo, N. Pezzotti, A. Signoroni. **On-the-fly automatic alignment and global registration of free-path collected 3D scans**. *2013 Digital Heritage International Congress*, 2013. [PDF](publications/2013_On-the-fly_automatic_alignment_and_global_registration_of_freepath_collected_3D_scans.pdf)
* N. Pezzotti, F. Bonarrigo, A. Signoroni. **Boosting the Computational Performance of Feature-Based Multiple 3D Scan Alignment by iat-k-means Clustering**. *3D Imaging, Modeling, Processing, Visualization and Transmission (3DIMPVT)*, 2012. [PDF](publications/Boosting_the_computational_performance_of_feature_based_multiple_3D_scan_alignment_by_iat_k_means_clustering.pdf)


Blog Posts
===================

For a full list of blog posts, visit the [Archive](archive/)

<ul>
{% for post in site.posts limit:5 %}
     <li>{{ post.date | date_to_string }} - <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

I moved the blog from [blogger](http://diaryofatinker.blogspot.nl/) the 5th of October 2015. 
Old posts can contain layout problems.




