---
title: "The Art of Feature Selection"
output:
  html_document:  
    keep_md: true
    toc: true
    toc_float: true
    code_folding: hide
    fig_height: 6
    fig_width: 12
    fig_align: 'center'
    theme: 'journal'
    css: styles.css
---


While working on my senior project, in which I had to create both a regression and classification model, I realized it can be hard sometimes to select the right features for your model. In school, our instructors usually do that for us resulting in us working with datasets with a few columns, all of them important. However, outside of school we have to deal with messy datasets and lots of variables that often do not help our model's accuracy; not only that but with a higher number of variables comes a higher possible number of models. 

Although there are already pacakges and automated solutions that pick for us the best model, in this post I'll discuss with you general principles that can help us in the selection. 

<center>

![](post4-1.jpg)
</center>

## Introduction

A model is a simplification of reality designed to promote understanding of the problems we want to address. Therefore, the "art" of model building involves simplifying reality to help us understand the problem we want to solve.

But finding the middle ground where simplicity is useful is not always an easy task. Here I show you what you should take into account when building your model so as not to underestimate or overestimate.

## Understanding the Scenarios

There are three possible scenarios we can find when we are creating machine learning models: 

#### Underfitting Models

If you choose very few variables, you can get a poorly detailed model and get estimates that are biased.

When one or more important predictor variables are missing, the regression coefficients will be biased and so will the predictions be.

#### Correct Model 

If your model contains all the relevant predictors, including any necessary transformations and the interaction terms, you will have a model without problems and with precise estimates.

#### Overfitting Models 

If you choose a model with too many variables you will have an excessively specified model and the estimates will be imprecise. Also remember that the model becomes more complicated and difficult to understand than necessary.

<center>

![Remember models seek to simplify reality not reproduce it](post4-2.jpg)

</center>

## So What Now? 

#### Have a Clear Objective and Question in Mind

Knowing how you are going to use your regression model can help you a lot in the feature selection phase. What model do you need in order to answer your question?

* Do you have any particular predictors of interest? If so, make sure your final model includes them.
* Are you interested in predicting the answer? If so, then don't worry too much about multicollinearity.
* Are you interested in the effects that specific predictors have on the response? If so, you should be careful with multicollinearity.
* Are you interested in the most simple approach?

#### Identify All Possible Predictors 

Make sure to identify all the important possible predictors, if you don't consider them, there is no chance that they will appear in your final model.

#### Explore and Graph Your Data

Yes, it is an obvious step but many researchers underestimate it and it can make you throw hours of hard work overboard. Check if there are outliers and / or missing values, or errors in the database, uni- and bivariate. It will allow you to have a prior idea of the type of relationship that exists between the variables (linear or nonlinear, multicollinearity, etc.).



