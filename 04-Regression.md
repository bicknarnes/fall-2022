
# 04-Regression

* [04-Regression](https://colab.research.google.com/drive/1ahLWDnas4fhwvIcDX8WulpLuxI5Eccoo?usp=sharing)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG?usp=sharing)

### Goals

* Introduce statsmodels (applied to the advertising dataset)
* Introduce the scikit-learn estimator API 
* Model evaluation (ISLR Chapter 2) and hypothesis testing (ISLR Chapter 3) with linear regression

### Reading (for next week)

ISLR2 -- Chapter 4: Classification (read the sections listed below)

* Section 4.1 & 4.2
* Section 4.3 -- concepts only, don't worry about mathematical details
* Section 4.4 -- might be tough reading, so don't worry about details
  * Sections 4.4.1-3 -- LDA and QDA -- skim
  * Section 4.4.4 -- Naive Bayes -- concepts only, we'll be using this model
* Sections 4.5-4.8 -- Entirely optional (we won't be covering this material)

### Polling

* polleverywhere questions based on reading for this week 
* [poll](poll.md)

### Introduction to statsmodels

* [statsmodels.org](https://www.statsmodels.org/stable/index.html)
* statsmodels is a port of R-stylej statistics to Python
* there are two APIs -- DSL (Domain Specific Language) similar to R, and a numpy-friendly API
* [exercises](statsmodels.md)
* **STOPPED HERE ON TUESDAY**
* ISLR2 -- Section 2.1 -- What is Statistical Learning?
  * Y = f(X) + epsilon
    * Equation 2.1 (p16) relates Y, f(X) and epsilon
    * epsilon and f(X) are unknowns
  * Yhat = fhat(X) is an estimate of f(X)
    * Equation 2.2 (p17) defines our prediction Yhat of Y, which equals our estimate fhat(X) of f(X)
    * epsilon is irreducible error
  * Eqn 2.3 -- Reducible and irreducible error (p19)
    * we can reduce prediction error (MSE) by our choice of fhat
    * "irreducible error will always provide an upper bound on the accuracy of our prediction"
    * one way to assess model accuracy is to look at the residual, Y-fhat
      * you can think of the residuals is our estimate of epsilon
      * is there anything in the residuals that departs from random noise?
* A question you might ask: What's the distribution of the residuals?
  * [seaborn distributions](https://seaborn.pydata.org/tutorial/distributions.html)
    * "An early step in any effort to analyze or model data should be to understand how the variables are distributed."
  * Gaussian noise has a normal distribution
  * [seaborn boxplot](https://seaborn.pydata.org/generated/seaborn.boxplot.html)
    * "A box plot (or box-and-whisker plot) shows the distribution of quantitative data in a way that facilitates comparisons between variables or across levels of a categorical variable."
  * [seaborn histplot](https://seaborn.pydata.org/generated/seaborn.histplot.html#seaborn.histplot)
   * "A histogram is a classic visualization tool that represents the distribution of one or more variables by counting the number of observations that fall within discrete bins."
  * [seaborn displot](https://seaborn.pydata.org/generated/seaborn.displot.html)
    * Figure-level interface for drawing distribution plots onto a FacetGrid.
* Correlation matrix
  * A question you might ask: Are the predictors (features) correlated with one another?
    * R^2 = Rsquared is the square of the correlation
  * With numpy (from statsmodels example): [plot_corr](https://www.statsmodels.org/dev/generated/statsmodels.graphics.correlation.plot_corr.html) example
  * With pandas [DataFrame.corr()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.corr.html)

### Pandas gotchas

* [notebooks/04-pandas-gotchas.ipynb](notebooks/04-pandas-gotchas.ipynb)
* TL;DR: Don't suppress pandas warnings -- fix them!

### Introduction to scikit-learn

* References...
  * p343 in VanderPlas (pdf) or...
  * [05.02-Introducing-Scikit-Learn.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.02-Introducing-Scikit-Learn.ipynb)
    * This notebook introduces scikit-learn
    * Data as a table (should be familiar with this)
      * Cells 1-4 talk about the data model using the iris dataset
    * Introduces the scikit-learn "Estimator API"
    * Demo: simple linear regression in Cells 5-11 is worth reviewing
  * Publication: [Estimators API](https://arxiv.org/abs/1309.0238) (2013) -- arxiv.org
  * Two perspectives: ISLR2 & VanderPlas (statistics & CS)
    * VanderPlas is actually an astronomy PhD and contributor to scikit-learn
    * Authors of ISLR2 (notably Hastie & Tibshirani) instrumental with R (formerly S)
    * Physics and astronomy communities successfully leverage the CS perspective
    * Biotech community is a heavy R user
    * Others (fintech, BI) use both
  * Different perspectives/communities typically means different language/jargon
    * Predictors -- Feature Matrix
    * Response -- Target array
* [04-polynomial-regression.ipynb](notebooks/04-polynomial-regression.ipynb)
  * This notebook looks at polynomial regression in detail as prep for the bias-variance tradeoff discussion below.
  * Cell 10 in [05.03-Hyperparameters-and-Model-Validation.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.03-Hyperparameters-and-Model-Validation.ipynb) uses a scikit-learn pipline for polynomial regression, including `sklearn.pipline`

### Bias-variance tradeoff

* Investigate bias-variance tradeoff based on VanderPlas: [05.03-Hyperparameters and model validation](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.03-Hyperparameters-and-Model-Validation.ipynb)
* Implement polynomial regression with simulated datasets
* Revisit (with scikit-learn) the topics in Chapter 2 of ISLR2

[bias-regression.md](bias-regression.md)
