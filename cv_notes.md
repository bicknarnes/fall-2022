# cross-validation notes

* [05.03-Hyperparameter-And-Model-Validation](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.03-Hyperparameters-and-Model-Validation.ipynb)
* [3.1 Cross Validation](https://scikit-learn.org/stable/modules/cross_validation.html) -- scikit-learn.org

From Chapter 6 of ISLR2...

* We us resampling methods to investigate the bias-variance tradeoff
  * In reality, we don't know truth
  * In 04-Regression, we investigated bias-variance tradeoff with simulated data -- so we did know "truth"
* ISLR2 looks at three approaches to resampling: (1) validation (hold-out) set, (2) LOOCV, (3) k-fold cross validation
* (1) Validation set -- Figure 5.2 (p200) in ISR2
  * Produces a high variance estimate of test MSE
    * Test error rate can vary a lot depending on which training sample is used
    * Figure 5.2 (p200) rhs shows this -- MSE vs model complexity (learning curve) varies a lot
  * Also produces a high bias estimate of test MSE
    * Will tend to overestimate the test-error rate compared to a model that fits the entire dataset
    * That's because statistical methods tend to perform worse when trained on fewer observations
* (2) LOOCV -- Figure 5.4 (p202) in ISLR2
  * LOOCV has a couple advantages over validation set (see p201)
  * LOOCV has less bias
    * LOOCV tends not to overestimate test-error rate as much as validation set approach
  * LOOCV also has relatively little variation in MSE because it uses essentially the same training dataset
* (3) k-fold CV -- Figure 5.6 (p205)
  * Estimate of test MSE may not be accurate
  * However, CV provides the correct general shape
  * For model selection: we're more interested in getting the shape right with a validation curve (p205)
* Bias-variance tradeoff for k-fold CV (Section 5.1.4, p205)
  * a less obvious but potentially more important advantage of k-fold CV...
  * it often gives more accurate estimates of the test error rate than does LOOCV
  * This has to do with a bias-variance trade-off.
  * from the perspective of bias reduction, it is clear that LOOCV is to be preferred to k-fold CV.
  * But we most also consider a method's variance
  * k-fold CV has lower variance than LOOCV!
    * the mean of many highly correlated quantities has higher variance 
    * than does the mean of many quantities that are not as highly correlated
    * LOOCV is always using essentially the same data -- all estimates of test MSE are essentially the same
    * Therefore, test MSE from LOOCV has high variance!
    * But we haven't shown this with any of the figures in the text.
  * Typically, k-fold cross-validation uses k = 5 or k = 10
    * these values have been shown empirically to yield test error rate estimates that
    * suffer neither from excessively high bias nor from very high variance (p206)
* Cross-validation works just as well for Classification (Section 5.1.5, p206-208)
  * Instead of MSE -- use the error rate (Eqn 5.4, p206)
  * For model selection: Figure 5.8 again shows that k-fold CV produces the right shape
  * Note: Figure 5.8 shows "true test MSE" and "true training MSE" -- these are different from irreducible MSE
  * You can see from Figure 5.7 (p207) that the true MSE associated with the Bayes decision boundary
    * The Bayes decision boundary has a lower training MSE than any of the fitted models
