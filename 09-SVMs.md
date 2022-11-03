
# 09-SVMs

* PCR & Random forests
* PCA and dimensionality 
* SVMs

## Project guidance

* [guidance.md](guidance.md)

## Reading (for next week)

* ISLR2 -- Chapter 12, Section 12.1: Unsupervised learning
* ISLR2 -- Chapter 12, Section 12.2: Principal Components Analysis
  * This is review, believe it or not -- ISLR2 provides a statistical perspective on ideas we've seen before
* ISLR2 -- Chapter 12, Section 12.3: Missing values and matrix completion
  * Read this quickly -- it's important, but we won't spend time on it in class
* ISLR2 -- Chapter 12, Section 12.4: Clustering methods
  * This is worth a careful read -- we'll be working with some of these techniques

## Notebooks

* [07-principal components](https://colab.research.google.com/drive/1KPXIhCoPorVjtXIYLGt7m-ZAcHM8FK7X)
* [08-hitters-pcr-exercises](https://colab.research.google.com/drive/1WC4OMezM9ODK9Sd3bynD3FKqE7hy9wgy)
* [08-hitters-pca-exercises](https://colab.research.google.com/drive/1nlvqWiUbmKEAGVbpZ0ATc4EDX7FM1GxP)
* [08-hitters-forest-exercises](https://colab.research.google.com/drive/1-e8zj1w2cIkoF7pdYeA4QYRvNyU33z-S)
* [09-lfw-svc-exercises](https://colab.research.google.com/drive/12ihADKzQ3wAD5iRH9S0aBcLb4cahLsVT)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG)
* [poll everywhere](https://pollev.com/pbogden)

## In-class exercises: Hitters PCR

* [08-hitters-pcr-exercises](https://colab.research.google.com/drive/1WC4OMezM9ODK9Sd3bynD3FKqE7hy9wgy)
* [sklearn.pipeline.Pipeline API](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html)
* pipeline: StandardScaler -- PCA -- linear regression

## In-class exercises: Hitters PCA

* [08-hitters-pca-exercises](https://colab.research.google.com/drive/1nlvqWiUbmKEAGVbpZ0ATc4EDX7FM1GxP)

## In-class exercises: Hitters Forest

* [08-hitters-forest-exercises](https://colab.research.google.com/drive/1-e8zj1w2cIkoF7pdYeA4QYRvNyU33z-S)
* Trees are high variance (small changes in the data can cause large changes in the final estimate)
* Ensemble methods combining many trees (weak learners) to greatly improve tree acccuracy
* Bagging (bootstrap aggregating) reduces variance by averaging models trained on bootstrapped training datasets
* Random forests improve on bagging by tweaking the algorithm to "decorrelate" the trees
* Other ensemble-method algorithms grow trees sequentially modifying the data long the way by fitting residuals
* Each approach has an associated set of tuning parameters (hyperparameters).

## In-class exercises: Labeled Faces in the Wild SVC

* [09-lfw-svc-exercises](https://colab.research.google.com/drive/17WafaXFvHSgyGOws2FvhdFn6O4LEmXqP)
