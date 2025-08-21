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

This repository is a code companion to [Somasundaram et al. (arXiv:2410.00247)](https://arxiv.org/abs/2410.00247) and the Zenodo database located [here](https://doi.org/10.5281/zenodo.16878207). The latter contains large datasets used in this work. The Jupyter Notebooks provided here, along with the data in the Zenodo database, can be used to re-create the analyses of the paper and to generate the main figures.    

## Contents

 * The Jupyter Notebooks, `plot_*.ipynb`, are the main ingredients of this repository. Each notebook contains a brief description of the data it reads in, the analysis it performs, and the main figure(s) in the paper that it re-creates.
 * The `ML_files` folder holds the saved machine learning (ML) based emulators used in the analysis. The ML models are stored as `.pickle` files and can be read by the accompanying Jupyter Notebooks.
 * The `NICER` folder contains Likelihood weights for each GW170817 posterior EOS sample. Each file is labelled according to the name of the NICER pulsar (J0030,J0740,J0437) and the EOS model (2,5,7-parameter models).
 * The `PMM` folder stores the fit values of the matrix elements of the parametric matrix models (PMM) used in the paper. Each file is labelled according to the density at which the PMM is used. This folder also contains the training and validation data for the PMM, generated using third-order many-body perturbation theory.
 * The `compound_unc_samples` folder contains 70 EOS validation samples used to estimate the total compound uncertainty (neural network error + PMM error) of the emulators used in this work. These samples are used to generate Fig. 4.
 * The `figures` folder contains the main plots in this paper and the `source_data` folder stores the data that is plotted in the figures.

Additionally, this repository contains empty folders which are intended to hold large datafiles that can be downloaded from the accompanying [Zeondo databse](https://doi.org/10.5281/zenodo.16878207). These datasets are required to run some of the Jupyter Notebooks. These folders are:
 * `Full_PE_results`: EOS posterior samples obtained from parameter estimation for third-generation detectors, performed under the zero-noise approximation.
 * `GW170817`: EOS posterior samples obtained from our GW170817 analysis.
 * `Injection_results`: EOS posterior samples for third-generation detectors, obtained under the Fisher Matrix approximation.
 * `samples`: Training and validation data for the neural network emulators. 

## Acknowledgements

The paper, along with its accompanying data and data analysis notebooks, has been approved for unlimited release and assigned LA-UR-24-29187. We thank C.L. Armstrong, K. Godbey, and P. Giuliani for feedback about the implementation of the PMM. We further thank D. Brown, C. Capano, C. Forssen, K. Hebeler, and W.G. Jiang for useful discussions. We also thank the Institute for Nuclear Theory at the University of Washington for its kind hospitality and stimulating research environment.

R.S. acknowledges support from the Nuclear Physics from Multi-Messenger Mergers (NP3M) Focused Research Hub which is funded by the National Science Foundation under Grant Number 21-16686, and from the Laboratory Directed Research and Development program of Los Alamos National Laboratory under project number 20220541ECR.
I.S. and A.S. were supported in part by the European Union's Horizon 2020 research and innovation programme (Grant Agreement No. 101020842).
S.D., A.E.D., and I.T. were supported by the Laboratory Directed Research and Development program of Los Alamos National Laboratory under project number 20230315ER.
A.E.D. was also supported in part by the U.S. Department of Energy, Office of Science, Office of Workforce Development for Teachers and Scientists (WDTS) under the Science Undergraduate Laboratory Internships Program (SULI).
I.T. was also supported by the U.S. Department of Energy, Office of Science, Office of Nuclear Physics, under contract No. DE-AC52-06NA25396, by the U.S. Department of Energy, Office of Science, Office of Advanced Scientific Computing Research, Scientific Discovery through Advanced Computing (SciDAC) NUCLEI program, and by the Laboratory Directed Research and Development program of Los Alamos National Laboratory under project numbers 20220541ECR.
Y.D. was supported by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) – Project-ID 279384907 – SFB 1245.
P.L. is supported by the Natural Sciences \& Engineering Research Council of Canada (NSERC). Research at Perimeter Institute is supported in part by the Government of Canada through the Department of Innovation, Science and Economic Development and by the Province of Ontario through the Ministry of Colleges and Universities.
Computational resources have been provided by the Los Alamos National Laboratory Institutional Computing Program, which is supported by the U.S. Department of Energy National Nuclear Security Administration under Contract No. 89233218CNA000001, and by the National Energy Research Scientific Computing Center (NERSC), which is supported by the U.S. Department of Energy, Office of Science, under contract No. DE-AC02-05CH11231, using NERSC awards NP-ERCAP-m3319 and NP-ERCAP-m4338.
I.S. and A.S. gratefully acknowledge the computing time provided on the high-performance computer Lichtenberg II at the TU Darmstadt. This is funded by the German Federal Ministry of Education and Research (BMBF) and the State of Hesse. I.S. and A.S. also gratefully acknowledge the Gauss Centre for Supercomputing e.V. (www.gauss-centre.eu) for funding this project by providing computing time on the GCS Supercomputer JUWELS~\cite{JUWELS} at Jülich Supercomputing Centre (JSC).

## Authors contributions:

R. Somasundaram and I. Svensson share first authorship. 
Conceptualization: RS, IS, PL, AS, IT; 
Methodology: RS, IS, SD, PL, AS, IT; 
Data curation: RS, IS, SD, PL; 
Software: RS, IS, SD, AED, YD, PL; 
Validation: RS, IS, SD, AED, YD, PL, AS, IT; 
Formal analysis: RS, IS, SD, AED, PL, AS, IT; 
Resources: IS, SD, PL, AS, IT; 
Funding acquisition: SD, PL, AS, IT; 
Project administration: RS, IS, PL, AS, IT; 
Supervision: RS, AS, IT; 
Visualization: RS, IS, AED, PL; 
Writing–original draft: RS, IS, YD, PL, AS, IT; 
Writing–review and editing: RS, IS, SD, AED, YD, PL, AS, IT.
