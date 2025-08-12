# Inferring three-nucleon couplings from multi-messenger neutron-star observations

**Rahul Somasundaram<sup>1,2</sup>, Isak Svensson<sup>3,4,5</sup>, Soumi De<sup>2</sup>, Andrew E. Deneris<sup>6</sup>, Yannick Dietz<sup>3,4</sup>, Philippe Landry<sup>7,8</sup>, Achim Schwenk<sup>3,4,5</sup>, Ingo Tews<sup>2</sup>**

**<sup>1</sup>Department of Physics, Syracuse University, Syracuse, NY 13244, USA**

**<sup>2</sup>Theoretical Division, Los Alamos National Laboratory, Los Alamos, NM 87545, USA**

**<sup>3</sup>Technische Universitat Darmstadt, Department of Physics, 64289 Darmstadt, Germany**

**<sup>4</sup>ExtreMe Matter Institute EMMI, GSI Helmholtzzentrum fur Schwerionenforschung GmbH, 64291 Darmstadt, Germany**

**<sup>5</sup>Max-Planck-Institut fur Kernphysik, Saupfercheckweg 1, 69117 Heidelberg, Germany**

**<sup>6</sup>Computer, Computational, and Statistical Sciences Division, Los Alamos National Laboratory, Los Alamos, NM 87545, USA**

**<sup>7</sup>Canadian Institute for Theoretical Astrophysics, University of Toronto, Toronto, Ontario M5S 3H8, Canada**

**<sup>8</sup>Perimeter Institute for Theoretical Physics, Waterloo, Ontario N2L 2Y5, Canada**

## Introduction

This repository is a code companion to [Somasundaram et al. (arXiv:2410.00247)](https://arxiv.org/abs/2410.00247) and the Zenodo database (XXXX). The latter contains the large datasets used in this work. The Jupyter Notebooks provided here, along with the data in the Zenodo database, can be used to re-create the analysis of the paper and to generate the main figures. 

## Contents

 * The Jupyter Notebooks, `plot_*.ipynb`, are the main ingredients of this repository. Each notebook contains a brief description of the data it reads in, the analysis it performs, and the main figure(s) in the paper that it re-creates.
 * The `ML_files` folder holds the saved machine learning (ML) based emulators used in the analysis. The ML models are stored as `.pickle` files and can be read by the accompanying Jupyter Notebooks.
 * The `NICER` folder contains Likelihood weights for each GW170817 posterior EOS sample. Each file is labelled according to the name of the NICER pulsar (J0030,J0740,J0437) and the EOS model (2,5,7-parameter models).
 * The `PMM` folder stores the fit values of the matrix elements of the parametric matrix models (PMM) used in the paper. Each file is labelled according to the density at which the PMM is used. This folder also contains the training and validation data for the PMM, generated using third-order many-body perturbation theory.
 * The `compound_unc_samples` folder contains 70 EOS validation samples used to estimate the total compound uncertainty (neural network error + PMM error) of the emulators used in this work. These samples are used to generate Fig. 4.
 * The `figures` folder contains the main plots in this paper and the `source_data` folder stores the data that is plotted in the figures.


