
# 10-Unsupervised

* PCA with images
* Clustering
* K-Means and silhouette analysis

## Notebooks

* [07-principal-components-exercises](https://colab.research.google.com/drive/1KPXIhCoPorVjtXIYLGt7m-ZAcHM8FK7X)
* [09-lfw-svm-exercises](https://colab.research.google.com/drive/12ihADKzQ3wAD5iRH9S0aBcLb4cahLsVT)
* [10-kmeans-digits-exercises](https://colab.research.google.com/drive/1WVESQgYXcaa8MTfedzionJk2j8OpKOBP)
* [10-learning-faces-exercises](https://colab.research.google.com/drive/1SiToIlQDKaSEqOqT1Brb4SvtBv00x3Y0)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG)
* [poll everywhere](https://pollev.com/pbogden) 

## Reading (for next week)

Text analysis next week, so read and try out the text-analysis sections in the following VanderPlas notebooks...

* [05.05-Feature-Engineering](https://github.com/jakevdp/PythonDataScienceHandbook/tree/master/notebooks)
* [05.05-Naive-Bayes](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.05-Naive-Bayes.ipynb)

## diamonds

* ONE-HOT ENCODING -- drop=first!!
* Debugging your data -- visualizing pitfalls of the simple train/test split
* DRY

## Linear models -> Trees -> SVMs

* ISLR2 Section 6.4 -- Considerations (of linear models) in higher dimensions
  * Most traditional statistical techniques for regression and classification are intended for the low-dimension, `n<<p`
  * The reasons are historical, related to data-collection technology -- linear models are too flexible when `n<<p`
  * Cp, AIC, BIC are no longer applicable; forward stepwise selection, ridge regression, lasso and PCR become useful
  * But interpretation of results can be problematic -- p-values, $R^2$ and other traditional metrics are inappropriate
* ISLR2 Ch 8 -- Trees
  * trees are simple and useful for interpretation, divide the feature space into nonlinear regions
  * simple trees are typically not competitive with other methods seen already
  * highly nonlinear ensembles (bagging, random forests, boosting, etc.) improve results, but lose interpretability
* ISLR2 Ch 9 -- SVMs
  * developed in the CS community in 90s, performed quite well at the time, and were thought to be different at the time
  * SVC is a maximum-margin classifier that can make mistakes; SVM is an SVC extended to nonlinear class boundaries
  * SVM kernels provide an efficient computational approach to increasing the feature space to deal with nonlinearities
  * SVM is not unique in this approach, and SVMs use the loss + penalty concept to control bias-variance tradeoff
* Thanks to the scikit-learn estimators API, these techniques are largely interchangeable

## PCA (review)

* PCA -- SVD -- dimensionality reduction, unsupervised learning, and (to a lesser extent, as we'll see) clustering
* VanderPlas -- In Depth: PCA (p431)
* [05.09-Principal-Component-Analysis.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.09-Principal-Component-Analysis.ipynb)
  * We've seen PCA for dimensionality reduction with linear models in high dimensions.
  * We'll see it act as a clustering method with text (e.g., LSA with the 20 NewsGroups)
  * Performs fairly well as a clustering method when the features are uncorrelated
  * Now we'll compare it with other methods specifically oriented toward clustering

## lfw-svm

* exercises

## Manifold Learning

* [05.10 Manifold Learning](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.10-Manifold-Learning.ipynb)
* "Some thoughts on manifold learning" (VanderPlas, p455)...
  * In practice, manifold learning techniques tend to be finicky
  * They are rarely used for anything more than simple qualitative visualization of high-dimensional data.
* t-SNE
  * For data that is highly clustered, t-distributed stochastic neighbor embedding (t-SNE) seems to work very well.
  * VanderPlas discusses t-SNE (right after Cell 15) the comparison with PCA

## K-Means

* VanderPlas -- In Depth: K-Means (p462)
* [05.11-K-Means.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.11-K-Means.ipynb)
  * Clustering optimizes division/discrete labeling of a groups of features
  * K-Means is a simple model to understand:
    * Data features comprised of cluster "centers', which are the arithmetic means of all the points in a clusters
    * Each point is closer to its own cluster center than to the others
  * Expectation-Maximimization -- a simple learning algorithm to implement:
    * Guess a set of cluster centers
    * Repeat until converged...
      * E-step -- Assign points to the closest center
      * M-step -- Set the cluster centers to the mean
  * Caveats
    * No guarantee of finding the global optimum fit
    * You must specify the optimal value of "k" 
* How do you choose K?
  * [Silhouette analysis](https://scikit-learn.org/stable/auto_examples/cluster/plot_kmeans_silhouette_analysis.html)
    * This scikit-learn demo uses make_blobs -- nice complement to VanderPlas's description using make_blobs
  * [silhouette_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html)
  * [silhouette coefficient](https://scikit-learn.org/stable/modules/clustering.html#silhouette-coefficient) defined
  * Digits dataset -- does reasonably well (0.79) without labels!
    * Does even better if you pre-process with t-SNE!

## K-means

* [10-kmeans-digits-exercises](https://colab.research.google.com/drive/1WVESQgYXcaa8MTfedzionJk2j8OpKOBP)

## learning curves

* [10-learning-faces-exercises](https://colab.research.google.com/drive/1SiToIlQDKaSEqOqT1Brb4SvtBv00x3Y0)

## Generative Models

* "Generative" models can generate new data instances
* Contrast with "discriminative" models that discriminate between different classes/types/groups of data
* Gaussian Mixture Model (GMM) -- a generative model that combines many Gaussian models
* VanderPlas has an extended discussion of GMMs
  * In Depth: Gaussian Mixture Models (p476)
  * [05.12-Gausian-Mixtures.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.12-Gaussian-Mixtures.ipynb)
  * Motivates GMMs by examining weeknesses of k-Means
    * clusters should be "circular"
    * clusters shouldn't overlap
  * Introduces GMMs with make_blobs
  * Demonstrates GMM with the half-moons dataset
  * Demonstrates GMM with dimension-reduced (using PCA) version of digits
