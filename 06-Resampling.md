
# 06 -- Resampling

## Projects

* [projects_update.md](projects_update.md)

## hw-flights

* folks who did database queries for Q2 got a similar result -- but different from the pandas/CSV solution
  * major award to the person who figures it out what's going on
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

## validation curves

* [05.03-Hyperparameters-and-Model-Validation.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.03-Hyperparameters-and-Model-Validation.ipynb) -- VanderPlas
  * Holdout sets
  * Validation curves (based on holdout sets -- since we don't know truth -- to determine the best model)
  * Learning curves (to determine the right number of samples)
* [06-validation-curves.ipynb](https://colab.research.google.com/drive/18FU3wLaqqDssxz7768dUil-g1bsLTNSk?usp=sharing)
* Exercises: Reproduce the qualitative features in Figure 5.6 of ISLR2 (204)
  * And related Figures 2.9 (p31), 2.10 (p33) & 2.11 (p34) of ISLR2
