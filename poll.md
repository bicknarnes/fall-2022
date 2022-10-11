# Poll

# 05-logreg-iris

How many mistakes does each model make?

* QUESTION 1 -- Which feature has separable classes for setosa and versicolor?
  * sepal_length, sepal_width, or **petal_length**
* QUESTION 2 -- Logistic regression with one-vs-rest
  * ANSWER: 27
* QUESTION 3 -- Gaussian Naive Bayes
  * ANSWER: 32
* QUESTION 4 -- KNN
  * ANSWER: 23
* QUESTION 5 -- KNN with k = 1
  * ANSWER: 12

# 05-classification

* QUESTION 1 -- Refer to Figure 4.4 (p144) of ISLR2, if you measure x=2, to which class does it belong?
  * green
  * **red**
  * DISCUSSION: Look at the horizontal axis and pick the largest probability
* QUESTION 2 -- Refer to Figure 4.10 (p1457) of ISLR2, given a new measurement: x = (0.4, 1.5, 1) to which class does it belong with highest probability?
  * **1**
  * 2
  * 3
  * DISCUSSION: This example is straight from the book where they plug values into Equation 4.30 to get
    * Pr(Y=1|X=x) = 0.944
    * Pr(Y=2|X=x) = 0.056
    * Note: there is no class "3"
* QUESTION 3 -- Referring to the Naive Bayes toy example in Section 4.4.4, suppose you have a measurement x = (0, 2, 3) -- to which class does it belong with highest probability?
  * Solution:
    * **1**
    * 2
    * 3     (note to self: there is no k=3)
    * None of the above
  * DISCUSSION: 
    * 0, 2, 3 are maximum values of f-hat for class k=1 (top row) in fig 4.10, p157 (you can see this by eye)
* QUESTION 4 -- Based on Figure 4.10 (p157) are the classes linearly separable?
  * Solution:
    * YES
    * **NO**
    * Impossible to tell from this figure
  * DISCUSSION:
    * linearly separable classes would have clearly distinguishable f-hat_1 & f-hat_2, there's overlap in all cases
    * that means you're likely to make mistakes, but the Bayes estimator will have the fewest mistakes
