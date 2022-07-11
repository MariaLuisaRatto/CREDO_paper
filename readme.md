---
title: 'CREDO: a friendly Customizable, REproducible, DOcker file generator'
tags:
  - Docker 
  - Reproducibility
  - Docker generator
  - User Iinterface 
authors:
  - name: Simone Alessandri'
    equal-contrib: 1 
    affiliation: 1
  - name: Rabellino Sergio
    equal-contrib: 2 
    affiliation: 2
  - name: Sandro Contaldo
    equal-contrib: 3 
    affiliation: 2
  - name: Maria Ratto
    equal-contrib: 3
    affiliation: 4
  - name: Gabriele Piacenti 
    equal-contrib: 3
    affiliation: 5
  - name: Qi Wang
    equal-contrib: 3 
    affiliation: 3
  - name: Marco Beccuti
    equal-contrib: 4
    affiliation: 2
  - name: Raffaele Adolfo Calogero
    equal-contrib: 4 
    affiliation: 4
  - name: Luca Alessandri
    equal-contrib: 5 
    affiliation: "3,4"
  - name: Author with no affiliation
    corresponding: true
    affiliation: 3
affiliations:
 - name: Politechnic of Turin, Torino, Italy
   index: 1
 - name: Department of Computer Science, University of Torino, Torino
   index: 2
 - name: Department of Pathology, Boston Children's Hospital, Harvard Medical School, Boston, MA, USA
   index: 3
 - name: Department of Molecular Biotechnology and Health Sciences, University of Torino, Torino
   index: 4
 - name: Molecular Biotechnology Center & Department of Life Sciences and Systems Biology, University of Turin, Torino, Italy
   index: 5
date: 11 July 2022
bibliography: paper.bib
aas-doi: 
aas-journal: JOSS The Journal of Open Source Software
---

# Abstract

Containerization is a way of wrapping software, OS libraries and dependencies required to create an application that can be consistently run using different computing environments. Among the containerization frameworks proposed in literature Docker and Singularity are those most widely used for Unix-like OS. Docker engine opened the way to reproducibility in the bioinformatics arena. Indeed, nowadays, Docker containerization is extensively used to facilitate the distribution of bioinformatics workflows. However, the proper creation of Docker images can be still a complex task requiring advance competencies in computer science. CREDO, a friendly Customizable REproducible DOckerfile generator, was developed to make easy the creation of a docker image. Indeed, CREDO can create docker images including different software stacks as pip, conda, bioconda, github, R-CRAN and Bioconductor packages according to the user ‘s needs. CREDO simplifies a lot the way of building docker images embedding R and Python packages and it provides extra level of reproducibility since allowing to store in a github all the elements requied to build from scratch a docker image. CREDO also support a friendly GUI making this tool an optimal solution for the efficient and easy generation of docker images for life scientists.

# Introduction

Reproducibility is a critical problem in the Bioinformatics field [1]. Docker engine [2] is an optimal tool to deal with reproducibility issues [3]. Nowadays, R [4] and Python [5] are the most used programming approaches to create bioinformatics tools [6] and workflows [7-9]. Furthermore, environment managers like Conda [10] and Bioconda [11] make easy the coexistence of different Python computing environments and they are frequently used within the bioinformatics community. On the R side, Bioconductor [12, 13] provides the deployment of software, providing rigorous and reproducible analysis of data from biological assays. Together with Github [14], Bioconductor represents one of the most used ways to distribute tools for the bioinformatics community.
Conda and Bioconda, together with packages distributed using Bioconductor and GitHub, can be exploited for the creation of complex docker containers [1, 6]. Although very useful, the above tools have some critical points: i. Bioconductor provides only version control for Bioconductor packages, underling software, e.g. R-CRAN packages, are not version controlled. ii. GitHub packages do not provide version control for the software inherited by the GitHub package and GitHub links might be unstable, e.g. a GitHub package can be deleted, moved or renamed without providing a stable tracking of the application updates. iii. Conda and Bioconda environment setup in Docker containers might not be easy to handle by not-expert people [15, 16].
In general, the creation of a Dockerfile, the core element for the creation of a docker image, including heterogeneous packages and environments (e.g. Bioconductor, Conda, etc.), is the most critical point for the generation of a docker image, being at the same time complex and time consuming, especially for not experienced people. CREDO, Customizable REproducible DOckerfile generator, software fixes some of the issues and difficulties described above, since it provides an easy way to build and customize a Dockerfile. CREDO provides at the same time a reproducible infrastructure and an easy way to distribute complete computing analysis workflow, e.g. docker images created by CREDO are perfectly suited to facilitate the distribution of complex code to reviewers or providing ready to go vignettes and tutorials (see supplementary information file). 
CREDO is organized in two modules namely CREDOengine and CREDOgui.

# Results
## CREDOengine

CREDOengine allows the construction of Dockerfile/s embedding Python and/or R. The architecture of CREDOengine is organized in three layers, Fig.1.
Layer 0 provides the possibility to create a Docker image embedding Python (0_PythonPackages) or R (0_RPackages). Layer 1 (1_mergeDocker) allows user to merge a Python Dockerfile with a R Dockerfile, previously generated at Layer 0. Layer 2, it provides the possibility to select various programming graphical interfaces (Jupyter lab, Jupyter notebook, Rstudio and Visual Studio), which can be accessed, in the built docker container, via web application (http://localhost:8888). Layer 3 (3_VMInDocker) configures the virtual environment to execute docker or singularity instances within a docker container, Fig. 1. This specific feature is useful in case the running docker container, requires executing the software embedded in another docker or in a singularity instance.
[[https://github.com/alessandriLuca/CREDO_paper/blob/main/Figs/figs1.png | width=100px]]

# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References
