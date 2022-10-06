
# Naive Bayes

VanderPlas's discussion of Naive Bayes classification is really nice.

* [05.05-Naive-Bayes.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.05-Naive-Bayes.ipynb)

The entire section complements the material in ISLR2. Some choice quotes...

## Bayes classifier

* In Bayesian classification, we're interested in finding the probability of a label given some observed features, which we can write as P(L|features).
* **Bayes's theorem tells us how to express this in terms of quantities we can compute more directly.**
* All we need now is some model by which we can compute P(features|L).
* Such a model is called a generative model because it specifies the hypothetical random process that generates the data.
* The discussion of **Gaussian** naive Bayes applies to quantitative predictors.
* The discussion of **multinomial** naive Bayes applies to categorical predictors.

## Naive assumption

* The naive Bayes classifier makes a single simplifying assumption
  * Within the "k"th class, the "p" predictors are independent (Equation 4.29, p155 of ISLR2)
* This assumption is powerful! (as discussed on p155 of ISLR2)
* For multivariate normal distribution, this means the off-diagonal terms in the matrix are zero.
  * Within each class, the predictors are assumed to have no association with each other.
* Even though the modeling assumptions are extreme, they often lead to decent results.

## When to use naive Bayes

Advantages...

* Extremely fast for both training and prediction
* Straightforward probabilistic prediction
* Often very easily interpretable
* Very few (if any) tunable parameters

Tend to perform well when

* The naive assumptions actually match the data (very rare in practice)
* Very well-separated categories, when model complexity is less important
* Very high-dimensional data, when model complexity is less important

These last two points are closely related because of the "curse of dimensionality."
