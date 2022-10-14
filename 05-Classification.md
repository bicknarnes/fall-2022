
# 05-Classification

## Reading (for next week)

* ISLR2 -- Chapter 5 -- Section 5.1 Resampling methods (cross-validation)

## Gapminder

* Review notebooks -- reproducibility (no jupyter notebooks) and my workflow
* Generic guidance...
  * Organize your repo so that your major results are presented in the README.md
  * Provide instructions for reproducing those results
  * Use one file with python code for each question and import reused code when appropriate (new)
  * No jupyter notebooks! (implicit)

## Notebooks


* [05-logreg-default-exercises.ipynb](https://colab.research.google.com/drive/1ks2RvShuGp2utTGNYFNs7Ybutq_-yR70?usp=sharing)
* [05-iris-logreg-exercises.ipynb](https://colab.research.google.com/drive/1r_T4-xAS-ynwwC2T_R9YUdicgkdV5Ihr?usp=sharing)
* [05-classification.ipynb](https://colab.research.google.com/drive/1q6eLG5cE8WoXcBBEFnekErU62W8kbCzU?usp=sharing)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG?usp=sharing)

## Projects (update)

* [projects_update.md](projects_update.md)
* Be ready to provide a pre-proposal with equivalent detail next week.

## For Thursday...

* Review reading for this week -- Naive Bayes

## bias-variance tradeoff (exercises)

* [04-bias-regression-exercises](https://colab.research.google.com/drive/1qowDu0rSlWqfYKDmHFzVUD-22IUIP7nv?usp=sharing)
* [bias-regression.md](bias-regression.md)

## STOPPED HERE on Tuesday

Note reading assignment for next week (above)

## classification -- why not linear regression?

* ISLR2 begins with 3-class problem...
* linear regression could be used if you made the three classes quantative
  * but you would be ordering the outcomes, which might not make sense
  * bottom line: "there is no natural way to convert a qualitative response variable with more than two levels into a quantitative response that is ready for linear regression"
* ISLR2 discusses numerical encoding for the binary qualitative response
  * you can order the 2 classes and use linear regression
  * "Curiously, it turns out that the classifications that we get if we use linear regression to predict a binary response will be the same as for the linear discriminant analysis (LDA) procedure we discuss in Section 4.4."
  * still, you won't get meaningful estimates of `Pr(Y|X)` with linear regression (model predicts values beyond 0 and 1)

## logistic regression with the default dataset

Topics

* 1-D logistic regression vs least-squares
* Reproduces analysis for credit-card default dataset in ISLR2, Section 4.5
* Introduces one-hot encoding
* [05-logreg-default-exercises.ipynb](https://colab.research.google.com/drive/1ks2RvShuGp2utTGNYFNs7Ybutq_-yR70?usp=sharing)

## logistic regression with the iris dataset

* relating cost functions -- least-squares regression and maximum likelihood
* multinomial logistic regression
* decision boundarie and confusion matrix
* [05-iris-logreg-exercises.ipynb](https://colab.research.google.com/drive/1r_T4-xAS-ynwwC2T_R9YUdicgkdV5Ihr?usp=sharing)

## naive Bayes

* [naive_bayes.md](naive_bayes.md)
* [poll.md](poll.md)
