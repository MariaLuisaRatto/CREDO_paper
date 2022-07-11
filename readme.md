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

`Gala` is an Astropy-affiliated Python package for galactic dynamics. Python
enables wrapping low-level languages (e.g., C) for speed without losing
flexibility or ease-of-use in the user-interface. The API for `Gala` was
designed to provide a class-based and user-friendly interface to fast (C or
Cython-optimized) implementations of common operations such as gravitational
potential and force evaluation, orbit integration, dynamical transformations,
and chaos indicators for nonlinear dynamics. `Gala` also relies heavily on and
interfaces well with the implementations of physical units and astronomical
coordinate systems in the `Astropy` package [@astropy] (`astropy.units` and
`astropy.coordinates`).

`Gala` was designed to be used by both astronomical researchers and by
students in courses on gravitational dynamics or astronomy. It has already been
used in a number of scientific publications [@Pearson:2017] and has also been
used in graduate courses on Galactic dynamics to, e.g., provide interactive
visualizations of textbook material [@Binney:2008]. The combination of speed,
design, and support for Astropy functionality in `Gala` will enable exciting
scientific explorations of forthcoming data releases from the *Gaia* mission
[@gaia] by students and experts alike.

# Mathematics

Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$
$a=2$
Double dollars make self-standing equations:

$$\Theta(x) = \left\{\begin{array}{l}
0\textrm{ if } x < 0\cr
1\textrm{ else}
\end{array}\right.$$

You can also use plain \LaTeX for equations
\begin{equation}\label{eq:fourier}
\hat f(\omega) = \int_{-\infty}^{\infty} f(x) e^{i\omega x} dx
\end{equation}
and refer to \autoref{eq:fourier} from text.

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
