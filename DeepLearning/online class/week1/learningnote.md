# Week 1 Deep Learning Notes

The first 30 episodes of the online course content are more fundamental. Mostly provide beginners with an understanding of deep learning.


The content of the first six episodes is mostly about background, so skip them.

## Episode 6: Binary Classification

Binary classification task, mainly to train a classifier that predicts the label (0/1) of the corresponding label based on the feature vector of the input image

## Episode 7: Logistic Regression

Logistic regression is used for binary classification tasks. It wraps the linear calculation result \(z=w^Tx+b\) of linear regression with a Sigmoid function, compressing the output to the interval \((0,1)\), which is interpreted as the **probability that the sample belongs to the positive class (\(y=1\))**.

$$z = w^T x + b$$
$$\hat y=\sigma(z)=\frac{1}{1+e^{-z}}$$
$$\hat y=\sigma(w^T x + b)$$

## Episode 8: Logistic Regression cost function

MSE is not used for logistic regression. Combined with the sigmoid function, the cost function becomes non-convex with many local minima. Gradient descent may get stuck at local optima. The cost function built with binary cross-entropy is convex and easier to optimize.

$$
\mathcal L(\hat y,y)=-\big(y\log\hat y + (1-y)\log(1-\hat y)\big)
$$

## Episode 9: Gradient Descent

Gradient descent updates parameters in the **negative gradient direction** of the cost function, to minimize the cost function.

$$
w := w-\alpha\frac{\partial J(w,b)}{\partial w}
\\
b := b-\alpha\frac{\partial J(w,b)}{\partial b}
$$

In episodes 10-15, it explain how to perform backpropagation, which is to first calculate the derivatives and then update the parameters using the gradient descent formula.**So we skip these episodes**

 ## Episode 16-19: Vectorization

In calculations, we should avoid explicit for-loops. Handwritten loops lack low-level optimizations and are much less efficient than vectorized encapsulated functions.

## Episode 20-24: Broadcast mechanism

Broadcasting simplifies code and supports vectorization; however, implicit dimension expansion can be error-prone, and rank-1 arrays are common pitfalls. Therefore, use two-dimensional vectors consistently when writing code to avoid such issues.

## Episode 25 :