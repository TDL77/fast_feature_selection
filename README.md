# fast_feature_selection

Genetic algorithms and CMA-ES (covariance matrix adaptation evolution strategy) for efficient feature selection

This is the companion repository for a series of two articles about efficient feature selection for regression models.

Link 1: TBD

Link 2: TBD

I've used the [House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data) dataset from Kaggle. After some processing, the dataset yields 213 features with 1453 observations.

The model used for regression is `statsmodels.api.OLS()`. The objective function used to select the best features is BIC, or the Bayesian Information Criterion - less is better.

Three feature selection techniques are explored:

- Sequential Feature Search (SFS) implemented via the [mlxtend](https://github.com/rasbt/mlxtend) library
- Genetic Algorithms (GA) implemented via the [deap](https://github.com/DEAP/deap) library
- Covariance Matrix Adaptation Evolution Strategy (CMA-ES) implemented via the [cmaes](https://github.com/CyberAgentAILab/cmaes) library

Results:

```
Run time (less is better):

SFS:    43.398 sec
GA:     161.511 sec
CMA-ES: 48.205 sec
```

```
Objective function (less is better):

SFS:    33708.9860
GA:     33705.5696
CMA-ES: 33703.0705
```
