# Introduction to Statistical Learning (Python)

## Chapter 1 Introduction

Background section. Nothing special.

## Chapter 2 Statistical Learning

### 2.1 What Is Statistical Learning?

1. `Input variables` $X$
    - Also known as `predictors`, `independent variables`, `features`, `variables`.
2. `Output variables` $Y$
    - Also known as `response`, `dependent variables`.
3. Understand actual underlying relationship $Y = f(X) + \epsilon$, by learning an estimation $\hat{Y} = \hat{f}(X)$.
4. $E(Y - \hat{Y})^2 = [f(X) - \hat{f}(X)]^2 + Var(\epsilon)$.
    - First part is called reducible error.
    - Second part is called irreducible error.
5. Higher the model flexibility (complexity), lower the model interpretability.
    - Complex model/algorithm is hard to fully interpret using human intuition.
6. `Supervised learning` means for all observations, we have an output variable value associated.
7. `Unsupervised learning` means we don't have such response variable that can supervise our statistical analysis, e.g. clustering problem.
8. Variable could be either quantitative or qualitative, i.e. numerical values vs. discrete labels. Problems with quantitative variables are referred to as `regression` problem, whereas problems with qualitative variables are referred to as `classification` problems.

### 2.2 Assessing Model Accuracy

1. `Mean squared error`
    - $MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{f}(x_i))^2)$
2. `Degrees of freedom` is a quantity that summarizes the flexibility of a curve.
3. $E(y_0 - \hat{f}(x_0))^2 = Var(\hat{f}(x_0)) + [Bias(\hat{f}(x_0))]^2 + Var(\epsilon)$, given test pair $(x_0, y_0)$.
    - Expected test MSE is the sum of variance of estimation function $\hat{f}(x_0)$, squared `bias` of $\hat{f}(x_0)$ and variance the irreducible error term $\epsilon$.
    - `Overfitting` is when the actual $f(X)$ is less flexible than estimation $\hat{f}(X)$, but yields a smaller test MSE. In other words, estimation $\hat{f}(X)$ *fits* training dataset too hard.
    - `Underfitting` is when the actual $f(X)$ is more flexible than estimation $\hat{f}(X)$, but yields a smaller test MSE. In other words, estimation $\hat{f}(X)$ is not learning enough from training set.
4. `Bayes classifier` is a classifier which assigns each observation the most likely class, given the predicators' values. In other words, it assigns $x_0$ the label $j$, if $Pr(Y=j|X= x_0)$ is the largest among all possible labels.
5. `K-nearest neighbors` algorithm is a classifier which for $x_0$, assigns label $j$ if majority of k nearest observations (i.e. k data points from training set which have least distance to $x_0$) have label $j$.  

## Chapter 3 Linear Regression