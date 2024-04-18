# Linear Regression
Linear regression is a fundamental supervised learning algorithm used for modeling the relationship between a dependent variable and one or more independent variables. This repository provides an overview of linear regression, its theoretical background, implementation in Python using scikit-learn, and applications.


## Introduction
Linear regression is a simple yet powerful algorithm used for predicting continuous outcomes. It assumes a linear relationship between the independent variables (features) and the dependent variable (target). The goal of linear regression is to find the best-fitting line that minimizes the difference between the observed and predicted values.

# Mathematical Formulation and Algorithm of Linear Regression

## Mathematical Formulation

### Simple Linear Regression

In simple linear regression, we have one independent variable X and one dependent variable y. 
The relationship between X and y is modeled using a straight line equation:

$$ y = mx + b $$

where:
$m$ is the slope of the line, representing the change in y for a unit change in X.
$b$ is the y-intercept, the value of y when X is zero.

### Multiple Linear Regression

In multiple linear regression, we extend the concept to multiple independent variables $$X_1, X_2, ..., X_n$$ influencing the dependent variable y. The relationship is modeled as:

$$ y = b_0 + b_1X_1 + b_2X_2 + ... + b_nX_n $$

where:
$b_0$ is the intercept term.
$b_1, b_2, ..., b_n$ are the coefficients of the independent variables.

## Algorithm: Ordinary Least Squares (OLS)

The Ordinary Least Squares method is a common approach for estimating the parameters of a linear regression model. It minimizes the sum of the squared differences between the observed and predicted values of $$ y $$.

### Cost Function

The cost function, also known as the loss function, measures the difference between the predicted values ( \hat{y}) and the actual values (y):

$$ J(b) = \frac{1}{2m} \sum_{i=1}^{m} (\hat{y}_i - y_i)^2 $$

where:
$m$ is the number of training examples.
$$ \hat{y}_i $$ is the predicted value for the $$ i $$th example.
$y_i$ is the actual value for the $$ i $$th example.

### Minimization

The goal is to find the values of the coefficients \b_0, b_1, ..., b_n that minimize the cost function J(b). This is typically achieved using optimization techniques like gradient descent.

### Gradient Descent

Gradient descent is an iterative optimization algorithm used to find the minimum of a function. In the context of linear regression, it updates the coefficients in the direction of the steepest descent of the cost function.

$$ b_j := b_j - \alpha \frac{\partial}{\partial b_j} J(b) $$

where:
$ \alpha $ is the learning rate, controlling the size of the steps taken during optimization.
$$ \frac{\partial}{\partial b_j} J(b) $$ is the partial derivative of the cost function with respect to the $ j$th coefficient.

### Closed-Form Solution

In simple linear regression, a closed-form solution exists for finding the optimal coefficients using matrix operations:

$$ b = (X^T X)^{-1} X^T y $$

where:
$X$ is the design matrix containing the independent variables.
$y$ is the vector of dependent variables.

## Conclusion

Linear regression is a simple yet powerful algorithm for modeling the relationship between variables. By understanding the mathematical formulation and algorithm behind linear regression, we can effectively estimate the parameters of the model and make predictions on new data.




## Applications
Economics: Predicting sales based on advertising expenditure.
Finance: Predicting stock prices based on market indicators.
Healthcare: Predicting patient outcomes based on clinical variables.
Engineering: Predicting energy consumption based on environmental factors.

![Ensemble](https://upload.wikimedia.org/wikipedia/commons/b/b5/Ensemble_Boosting.svg) 
image from wikipedia 
