# Bayesian_DP_Gibbs

## Markov Chain Monte Carlo Gibbs Sampling for Dirichlet Process Mixture Model

In this project, we applied a Bayesian modelling approach to categorical data that came from different latent populations with and without missing data, the typical setting researchers face in analyzing survey datasets. For each topic, we started with specifying the data generating process to obtain the simulated data, constructing the prior specifications for Bayesian analysis, and finally laying out the posterior full conditional distributions of unknown parameters suitable for Gibbs sampling to obtain Markov Chain Monte Carlo samples for further analysis. At the end of each topic, we made some comparison with the original datasets in terms of the marginal probability mass function (pmf) of different features and the mixing proportion of the unobserved latent variables controlling the population group assignments.

For frequentists, these can be achieved via Estimation-Maximization process (EM) while the latent variables here are called responsibilities for each observations. However, the EM process will result in the maximum likelihood point estimate and it is difficult to take into account uncertainty for those MLE estimates. In Bayesian paradigm, all unknown parameters can be quantified in term of uncertainty using the posterior distribution and, hence, the credible interval can be approximated via sampling.

**Keywords**: Mixture Model (MM), Dirichlet distribution and Dirichlet process (DP), Multinomial Mixture Model, Missing data imputation, Gibbs sampling, Blocked gibbs sampling, Dirichlet process mixture of products of multinomial distributions model (DPMPM)

## Objectives

Explore Blocked Gibbs Sampling process in Mixture of multinomial data modelling process
Identify label switching and how investigating marginal pmf is more suitable in ensure the quality of the sampling process
Perform missing data impuation under Bayesian paradigm with different missing data mechanisms: missing completely at ranomd (MCAR), missing at random (MAR), and missing not at random (MNAR)

## Dataset

Data used in this project is a simulated data from the generative process described in each file.

## Software and analytical approaches

All analysis programming is done using R. The statistical techniques covered in this repository includes Mixture of multinomial model, latent variable model, Bayesian modelling, blocked gibbs sampling (MCMC sampling approach), and missing data imputation.

Most of the gibbs samplers here were written without using any external sampling packages (from scratch) except for some comparisons made using NPBayesImputeCat package (Ref: https://cran.r-project.org/web/packages/NPBayesImputeCat/NPBayesImputeCat.pdf)

## File description

**01Dirichlet_1D**: The basic Multinomial model with Dirichlet prior in which no latent groups are imposed on the data generating process
**02Dirichlet_Mixtures**: Using Multinomial Mixture Model with gibbs sampling in which latent groups are imposed
**03Dirichlet_Mixtures_trials**: Same as 02 but instead of a categorical outcome, we have a multinomial trials for each features
**04Dirichlet_Mixtures_MultD**: Same as 02 but with multiple features with some association conditional on the latent variable
**05Dirichlet_Process_Mixtures**: Using Dirichlet process to avoid the necessity to prespecifying the number of latent groups/clusters. With this approach, we allow for theoretically infinite mixture model.
**06DP_Mixture_MAR**: Same as 05 but with data missing at random (MAR) and the goal is to impute the data while preserving the data statistical structure
**07DP_Imputation_MAR**: Same as 06 but instead of writing code from scratch, rely on NPBayesImputeCat package
**08DP_Mixture_MNAR**: Same as 05 but with data missing not at random (MNAR) and the goal is to impute the data while preserving the data statistical structure
**09DP_Imputation_MNAR**: Same as 08 but instead of writing code from scratch, rely on NPBayesImputeCat package
Authors

**Chayut Wongkamthong**, Duke University - Initial work
Acknowledgments

**Advisor**: professor Olanrewaju M. Akande Ph.D., Statistical Science, Duke University
