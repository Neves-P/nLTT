# nLTT <img src="pics/nLTT_sticker.png" align="right" width="180" />

[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/nLTT)](https://cran.r-project.org/package=nLTT)
[![](http://cranlogs.r-pkg.org/badges/grand-total/nLTT)]( https://CRAN.R-project.org/package=nLTT)
[![](http://cranlogs.r-pkg.org/badges/nLTT)](https://CRAN.R-project.org/package=nLTT)
  [![R-CMD-check](https://github.com/thijsjanzen/nLTT/workflows/R-CMD-check/badge.svg)](https://github.com/richelbilderbeek/nLTT/actions)

Branch|[![Travis CI logo](pics/TravisCI.png)](https://travis-ci.org)|[![AppVeyor logo](pics/AppVeyor.png)](https://www.appveyor.com)|[![Codecov logo](pics/Codecov.png)](https://www.codecov.io)
---|---|---|---
master|[![Build Status](https://travis-ci.org/thijsjanzen/nLTT.svg?branch=master)](https://travis-ci.org/thijsjanzen/nLTT)|[![Build status](https://ci.appveyor.com/api/projects/status/8seg4oj4bj68piff/branch/master?svg=true)](https://ci.appveyor.com/project/thijsjanzen/nLTT/branch/master)|[![codecov.io](https://codecov.io/github/thijsjanzen/nLTT/coverage.svg?branch=master)](https://codecov.io/github/thijsjanzen/nLTT/branch/master)
develop|[![Build Status](https://travis-ci.org/thijsjanzen/nLTT.svg?branch=develop)](https://travis-ci.org/thijsjanzen/nLTT)|[![Build status](https://ci.appveyor.com/api/projects/status/8seg4oj4bj68piff/branch/develop?svg=true)](https://ci.appveyor.com/project/thijsjanzen/nLTT/branch/develop)|[![codecov.io](https://codecov.io/github/thijsjanzen/nLTT/coverage.svg?branch=develop)](https://codecov.io/github/thijsjanzen/nLTT/branch/develop)

Repository for the R nLTT package

## Installing this package

Make sure you have the package `devtools` installed.

Then, from within R do, for the stable version:

```
devtools::install_github("thijsjanzen/nLTT")
```

For the bleeding-edge version:

```
devtools::install_github("thijsjanzen/nLTT", ref = "develop")
```

## What is the nLTT statistic?
The nLTT statistic is a likelihood free summary statistic to compare the similarity between two phylogenetic trees.  It calculates the distance between the lineage through time curves of the two trees, after normalizing the lineage through time curves with respect to the maximum number of lineages obtained in each tree, and with respect to the total time between the root and the tips of the tree (see also the wiki).

A more detailed description, and a detailed analysis of the performance of the nLTT statistic can be found in the following paper:

Janzen, Thijs, Sebastian Höhna, and Rampal S. Etienne. "Approximate Bayesian computation of diversification rates from molecular phylogenies: introducing a new efficient summary statistic, the nLTT." Methods in Ecology and Evolution 6.5 (2015): 566-575. [link](http://onlinelibrary.wiley.com/doi/10.1111/2041-210X.12350/full)

## What else does the package do?
Apart from providing functions that calculate the nLTT statistic, the nLTT package for R also provides functions to:
- plot the normalized Lineages-Through-Time plot for a single, or for multiple, trees
- calculate and plot the average Lineages-Through-Time plot for multiple trees
- estimate the parameters of a model for which the likelihood is known (for comparison), using MCMC (as used in the paper)
- estimate the parameters of a model for which no likelihood is available, using ABC-SMC (as used in the paper)

## Papers using the nLTT statistic

Shu Xie, Luis Valente, Rampal S. Etienne. A simple island biodiversity model is robust to trait dependence in diversification and colonization rates (2022) bioRxiv 2022.01.01.474685; doi: https://doi.org/10.1101/2022.01.01.474685


Francisco Richter, Thijs Janzen, Hanno Hildenbrandt, Ernst C. Wit, Rampal S. Etienne. Detecting phylodiversity-dependent diversification with a general phylogenetic inference framework (2021) bioRxiv 2021.07.01.450729; doi: https://doi.org/10.1101/2021.07.01.450729

Thijs Janzen, Folmer Bokma, Rampal S Etienne, Nucleotide Substitutions during Speciation may Explain Substitution Rate Variation, Systematic Biology (2021), syab085, https://doi.org/10.1093/sysbio/syab085

Pedro Santos Neves, Joshua W. Lambert, Luis Valente, Rampal S. Etienne. "The robustness of a simple dynamic model of island biodiversity to geological and eustatic change"
bioRxiv  (2021) 2021.07.26.453064; doi: https://doi.org/10.1101/2021.07.26.453064

Bilderbeek, RJC, Laudanno, G, Etienne, RS. Quantifying the impact of an inference model in Bayesian phylogenetics. Methods Ecol Evol. (2021); 12: 351– 358. https://doi.org/10.1111/2041-210X.13514

Hagen O, Flück B, Fopp F, Cabral JS, Hartig F, et al. (2021) gen3sis: A general engine for eco-evolutionary simulations of the processes that shape Earth’s biodiversity. PLOS Biology 19(7): e3001340. https://doi.org/10.1371/journal.pbio.3001340

Giardina F, Romero-Severson EO, Albert J, Britton T, Leitner T  "Inference of Transmission Network Structure from HIV Phylogenetic Trees". PLOS Computational Biology (2017) 13(1): e1005316. [link](https://doi.org/10.1371/journal.pcbi.1005316)

Janzen, Thijs, and Rampal Etienne. "Inferring the role of habitat dynamics in driving diversification: evidence for a species pump in Lake Tanganyika cichlids." bioRxiv (2017): 085431. [link](https://www.biorxiv.org/content/early/2017/06/07/085431)

Ibeh, Neke, and Stephane Aris-Brosou. "Estimation of sub-epidemic dynamics by means of Sequential Monte Carlo Approximate Bayesian Computation: an application to the Swiss HIV Cohort Study." bioRxiv (2016): 085993. [link](http://biorxiv.org/content/early/2016/11/07/085993)

McCloskey, Rosemary M., Richard H. Liang, and Art FY Poon. "Reconstructing contact network parameters from viral phylogenies." Virus evolution 2.2 (2016): vew029. [link](http://ve.oxfordjournals.org/content/2/2/vew029.abstract)

Janzen, Thijs, Sebastian Höhna, and Rampal S. Etienne. "Approximate Bayesian computation of diversification rates from molecular phylogenies: introducing a new efficient summary statistic, the nLTT." Methods in Ecology and Evolution (2015): 566-575. [link](http://onlinelibrary.wiley.com/doi/10.1111/2041-210X.12350/full)

## Acknowledgements

 * @franciscorichter: bug reporting

## I want to contribute!

See [CONTRIBUTING.md](CONTRIBUTING.md)

## Code of Conduct

See [code_of_conduct.md](code_of_conduct.md)
