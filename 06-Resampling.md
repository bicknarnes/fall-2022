
# 06 -- Resampling

## Reading (for next week)

ISLR2 -- Chapter 6.1-6.4: Model selection

* There's a fair amount of reading. Try to get the main concepts and don't get caught up in the math.
* You should try to understand the main points of subset selection, shrinkage methods.
* Skim the section on Cp, AIC, BIC, and Adjusted R2.
* Lasso and Ridge: How do they work? Why might you want to use one versus the other?
* If you're not familiar principal components, then read 6.3 for an introduction to the concepts.
* High dimensional situations. What does it mean to be high-dimensional? What are some problems that arise? 

## notebooks

* [05-iris-logreg-exercises.ipynb](https://colab.research.google.com/drive/1r_T4-xAS-ynwwC2T_R9YUdicgkdV5Ihr?usp=sharing)
* [06-cross-validation-exercises.ipynb](https://colab.research.google.com/drive/1IcW50M2yDkgDSDTooeYuLY7BQkzbm2Y1?usp=sharing)
* [06-validation-curves-exercises.ipynb](https://colab.research.google.com/drive/18FU3wLaqqDssxz7768dUil-g1bsLTNSk?usp=sharing)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG?usp=sharing)

## Projects

* [projects_update.md](projects_update.md)

## hw-flights

* folks who did database queries for Q2 got a similar result -- but different from the pandas/CSV solution
  * major award to the person who figures out what's going on
* several folks used groupby without any averaging operation 
* don't submit jupyter notebooks in github-classroom!

## log-reg iris

* cost function -- related to perceptron
* separable classes
* multiple classes and features
* decision boundaries for other models (one-vs-rest, Gaussian naive Bayes, KNN)
* [05-iris-logreg-exercises.ipynb](https://colab.research.google.com/drive/1r_T4-xAS-ynwwC2T_R9YUdicgkdV5Ihr?usp=sharing)
* [poll.md](poll.md)

## naive Bayes

* [naive_bayes.md](naive_bayes.md)
* [poll.md](poll.md)

##  cross validation

* [cv_notes.md](cv_notes.md)
* Figure 5.2 (p200) ISLR2 -- validation (hold-out) set
* Figure 5.3 (p202) ISLR2 -- LOOCV and 10-fold cross validation
* [06-cross-validation-exercises.ipynb](https://colab.research.google.com/drive/1IcW50M2yDkgDSDTooeYuLY7BQkzbm2Y1?usp=sharing)

## validation curves

* [05.03-Hyperparameters-and-Model-Validation.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.03-Hyperparameters-and-Model-Validation.ipynb) -- VanderPlas
  * Holdout sets
  * Validation curves (based on holdout sets -- since we don't know truth -- to determine the best model)
  * Learning curves (to determine the right number of samples)
* [06-validation-curves-exercises.ipynb](https://colab.research.google.com/drive/18FU3wLaqqDssxz7768dUil-g1bsLTNSk?usp=sharing)
* Exercises: Reproduce the qualitative features in Figure 5.6 of ISLR2 (p204)
  * And related Figures 2.9 (p31), 2.10 (p33) & 2.11 (p34) of ISLR2
