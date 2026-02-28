# MA-TabNet for Global Maternal Mortality Prediction

**MA-TabNet** is a missingness-aware deep tabular learning framework for predicting the **global maternal mortality ratio (MMR)** from country-level health and socioeconomic indicators.
The model is designed for **high-sparsity public health tabular data**, where missing entries are not treated as mere preprocessing artifacts, but as potentially informative signals reflecting structural differences in reporting capacity, surveillance continuity, and administrative infrastructure.

This repository accompanies our study on **Missingness-Aware TabNet (MA-TabNet)** and provides the implementation used for reproducible experiments on a global **country-year panel** constructed from publicly available data sources. The framework extends TabNet with a **distribution-aware selective masking (DASM)** strategy, which introduces missingness indicators only for variables with substantively high missingness, thereby preserving informative absence patterns while avoiding unnecessary dimensional expansion.

## Key Features

* **Missingness-aware tabular learning** for maternal mortality prediction
* **Distribution-aware selective masking (DASM)** to encode structural missingness
* **TabNet-based sequential attention** for interpretable feature selection
* **Country and continent embeddings** for modeling cross-national heterogeneity
* **Temporal validation protocol** for realistic year-ahead forecasting
* **Layered explainability pipeline**, including attention analysis, feature importance, SHAP, permutation importance, and partial dependence plots

## Study Motivation

Predicting maternal mortality at the global scale is challenging because country-level data are often **heterogeneous, incomplete, and temporally uneven**. In many settings, missing values arise not from random noise but from **systematic limitations in reporting systems and institutional capacity**. MA-TabNet was developed to explicitly model this structure, allowing the learning algorithm to use missingness patterns as part of the signal rather than discarding them as nuisance.

## Repository Scope

This repository is intended to support:

* **Model transparency**
* **Experimental reproducibility**
* **Methodological inspection of MA-TabNet**
* **Supplementary material for the associated manuscript**

It includes the implementation of preprocessing, selective masking, model training, temporal validation, and explainability analyses used in the study.

## Method Overview

The proposed framework consists of four main stages:

1. **Country-year panel construction** from publicly available global health and nutrition data
2. **Structural missingness handling** via selective missingness indicators and median imputation for numerical stability
3. **MA-TabNet training** with entmax-based sequential attention and Bayesian hyperparameter optimization
4. **Explainability and diagnostic analysis** through intrinsic and post hoc interpretation methods

## Intended Use

MA-TabNet is designed as a **decision-support modeling framework** for maternal health monitoring and related global health prediction tasks involving **sparse, incomplete, and policy-relevant tabular data**. It is especially suited for settings in which the observation pattern itself may carry meaningful information about institutional or reporting conditions.

## Citation

If you use this repository or build upon this framework, please cite the associated manuscript.

---

**Keywords:** maternal mortality ratio, TabNet, missingness-aware learning, structural missingness, global health AI, interpretable deep learning, tabular prediction
