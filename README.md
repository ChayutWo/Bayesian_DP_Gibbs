# Bayesian_DP_Gibbs
Blocked Gibbs Sampling for Dirichlet Process Mixture Model

In this project, we applied a Bayesian modelling approach to categorical data that came from different latent populations with and without missing data, the typical setting researchers face in analyzing survey datasets. For each topic, we started with specifying the data generating process to obtain the simulated data, constructing the prior specifications for Bayesian analysis, and finally laying out the posterior full conditional distributions of unknown parameters suitable for Gibbs sampling to obtain Markov Chain Monte Carlo samples for further analysis. At the end of each topic, we made some comparison with the original datasets in terms of the marginal probability mass function (pmf) of different features and the mixing proportion of the unobserved latent variables controlling the population group assignments.  

For frequentists, these can be achieved via Estimation-Maximization process (EM) while the latent variables here are called responsibilities for each observations. However, the EM process will result in the maximum likelihood point estimate and it is difficult to take into account uncertainty for those MLE estimates. In Bayesian paradigm, all unknown parameters can be quantified in term of uncertainty using the posterior distribution and, hence, the credible interval can be approximated via sampling.

**Keywords:** Mixture Model (MM), Dirichlet distribution and Dirichlet process (DP),  Multinomial Mixture Model, Missing data imputation, Gibbs sampling, Blocked gibbs sampling, Dirichlet process mixture of products of multinomial distributions model (DPMPM)

## Objectives

1. Explore Blocked Gibbs Sampling process in Mixture of multinomial data modelling process
2. Identify label switching and how investigating marginal pmf is more suitable in ensure the quality of the sampling process
3. Perform missing data impuation under Bayesian paradigm with different missing data mechanisms: missing completely at ranomd (MCAR), missing at random (MAR), and missing not at random (MNAR)

## Dataset

Data used in this project is a simulated data from the generative process described in each file.

## Software and analytical approaches

All analysis programming is done using R. The statistical techniques covered in this study includes 

## File description

* 01Dirichlet_1D:
* 02Dirichlet_Mixtures:
* 03Dirichlet_Mixtures_trials:
* 04Dirichlet_Mixtures_MultD: 
* 05Dirichlet_Process_Mixtures: 
* 06DP_Mixture_MAR:
* 07DP_Imputation_MAR: 
* 08DP_Mixture_MNAR: 
* 09DP_Imputation_MNAR: 

## Authors

* **Chayut Wongkamthong, Duke University** - *Initial work* 

## Acknowledgments

Advisor: professor Olanrewaju M. Akande Ph.D., Statistical Science, Duke University
