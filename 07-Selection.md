
# 07-Selection

* curse of dimensionality
* knn vs logistic regression -- curse demo and the importance of scaling
* model selection -- selection, regularization, PCA and PCR

## Notebooks

* [07-curse-of-dimensionality-exercise.ipynb](https://colab.research.google.com/drive/1nwULWhFqm72fIRBULSapPsqGW3Z6niXk?usp=sharing)
* [07-curse-demo-exercises.ipynb](https://colab.research.google.com/drive/1et-iTTFBAEtuaouxQkKhLVu8Q9hqG6hK?usp=sharing)
* [07-iris-pipeline-exercises.pynb](https://colab.research.google.com/drive/1gkpExUJjHfmuNDaRkUqznZ2GxaZxCHJT?usp=sharing)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG?usp=sharing)
* [poll everywhere](https://pollev.com/pbogden)

## Pre-proposals

* See comments in Canvas
* Next step: [feasibility](feasibility.md) -- due next week
* [Computer-vision position announcement](cv_position.md)

## In-class exercise: Curse of dimensionality

* High dimensional models incur all sorts of problems
  * KNN illustrates the issues
  * Recall KNN estimate of Bayes decision boundary in Figure 2.14 (p40)
* [exercises.md](exercises.md)

## In-class exercises: Curse demo

* [exercises.md](exercises.md)

## Metrics for choosing the optimal model

* Notes from "Section 6.1.3 Choosing the optimal model"
* Training MSE can't be used for model selection
  * Training MSE generally underestimates test MSE
  * Training MSE is a bad estimate of MSPE because it always decreases as the number of predictors increases
  * Test MSE is an estimate of MS Prediction Error (MSPE)
* Metrics: Cp, AIC, BIC, Adjusted R^2 (p234)
  * All of these are metrics for estimating MSPE that can aid in model selection
  * [Cp (Mallows Cp)](https://en.wikipedia.org/wiki/Mallows%27s_Cp)
    * Cp is an estimate of MSPE defined to address overfitting with regression
    * Cp is a sample statistic -- Cp thus depends on the model -- the model could produce a poor estimate of MSPE
    * Wikipedia article identifies various limitations of Cp
  * [AIC (Akaike Information Criterion)](https://en.wikipedia.org/wiki/Akaike_information_criterion)
    * AIC is a metric for MSPE designed to address overfitting for a large class of models fit by maximum likelihood
    * AIC adds a penalty term that increases with the number of predictors
    * Cp and AIC are similar for Gaussian errors -- for least-squares models they're proportional
  * [BIC (Bayes Information Criterion)](https://en.wikipedia.org/wiki/Bayesian_information_criterion)
    * BIC and AIC are closely related -- they both add penalties for # of predictors
    * With BIC, penalty is ln(n)k compared to 2k for AIC, where k = # of predictors (ISLR2 uses "d" instead of "k")
    * ln(k)k > 2k for ln(k) > 2, i.e., for k > exp(2) = 7.4...
    * BIC places a larger penalty on the number of predictors than AIC when k > 7
  * [Adjusted R^2](https://en.wikipedia.org/wiki/Coefficient_of_determination#Adjusted_R2)
    * Another metric -- wikipedia def'n uses residual & total "degrees of freedom"; ISLR2 uses (n-d-1) & (n-1)

## In-class exercises: Iris pipeline

* [exercises.md](exercises.md)

## Dimensionality reduction

* [07-principal-components.ipynb](https://colab.research.google.com/drive/1Xc5SNhD9NY-4IGE-mGdPu8mdpPTxHIIf?usp=sharing)
