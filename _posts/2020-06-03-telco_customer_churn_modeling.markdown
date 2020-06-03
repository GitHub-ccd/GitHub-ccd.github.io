---
layout: post
title:      "Telco Customer Churn modeling"
date:       2020-06-03 16:05:54 -0400
permalink:  telco_customer_churn_modeling
---

__How to retain Telco customers via machine learning__


## Introduction

Build a binary classifier to predict whether a customer will ("soon") stop doing business with Telco, a telecommunications company. The dataset of customer record with both numerical and categorical data is considered this project. 


## Objectives

- Understand all required aspects of the features
- clean data 
- choose classifiers 


## The Project

The main goal of this project is to create a classification model. For this project you have the choice to either:

- choose a data set from a curated list
- choose your own data set _outside_ of the curated list. 

The data guidelines for either option are shown below

For this project, you're going to select a dataset of your choosing and create a classification model. You'll start by identifying a problem you can solve with classification, and then identify a dataset. You'll then use everything you've learned about Data Science and Machine Learning thus far to source a dataset, preprocess and explore it, and then build and interpret a classification model that answers your chosen question.

## Methodology and code origanization
![](https://raw.githubusercontent.com/GitHub-ccd/dsc-mod-3-project-v2-1-onl01-dtsc-ft-030220/master/img/osemn.png)
1. **1-Obtain.ipynb**: Data loading and initial visualization and exploration of target. outliers. 
2. **2-Scrub.ipynb**: Cleaning data and verifying integrety. initial feature engineering based on domain expertiese. Assess the degree of multicolliniarity and possible ways of handling it.  
3. **3-EDA.ipynb**: visualization and exploration of features in relation to the target. 
4. **4-Model.ipynb**: Build a baseline model. Handel class imballance. Build several classification models. Compare evaluation matrices and bias variance tradoff off amoung them. Tune hyper parameters to achieve highest possible accuracy for acceptable level of recall. Prepare a suitable feature engineering strategy and impliment it to the best possible models.  
5. **5-iNterpret.ipynb**: Further analyse the most important features obtained from the best model. Draw conclusion from the model and the predicted features. Build necessary figures to complement recommendation to Telco 

## final model summary
![](https://raw.githubusercontent.com/GitHub-ccd/dsc-mod-3-project-v2-1-onl01-dtsc-ft-030220/master/img/RandForest_feature_importance.png)

## comparison of churn prediction 
![](https://raw.githubusercontent.com/GitHub-ccd/dsc-mod-3-project-v2-1-onl01-dtsc-ft-030220/master/img/model_comparison.png)

