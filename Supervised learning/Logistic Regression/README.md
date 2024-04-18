# Logistic Regression

## Introduction

Logistic regression is a popular statistical method used for binary classification tasks. Unlike linear regression, which predicts continuous outcomes, logistic regression predicts the probability of an event occurring based on input features. This README provides an overview of logistic regression, including its mathematical background, algorithm, advantages, disadvantages, and applications.

## Mathematical Background

### Binary Logistic Regression

In binary logistic regression, the goal is to model the probability that an instance belongs to a particular class. The logistic function (also known as the sigmoid function) is used to map the output of the linear combination of input features to a probability between 0 and 1:

$$
P(y=1|\mathbf{x};\mathbf{w}) = \frac{1}{1 + e^{-(\mathbf{w}^T\mathbf{x} + b)}}
$$

where:
- $P(y=1|\mathbf{x};\mathbf{w})$ is the probability that $y$ equals 1 given input $\mathbf{x}$ and model parameters $\mathbf{w}$.
- $\mathbf{w}$ is the weight vector.
- $\mathbf{x}$ is the input feature vector.
- $b$ is the bias term.

The logistic function $\sigma(z)$ is defined as:

$$
\sigma(z) = \frac{1}{1 + e^{-z}}
$$

where $z = \mathbf{w}^T\mathbf{x} + b$.

The logistic function maps any input $z$ to a value between 0 and 1. Therefore, $P(y=1|\mathbf{x};\mathbf{w})$ represents the probability that the output $y$ is 1 given the input $\mathbf{x}$ and model parameters $\mathbf{w}$.

### Optimization: Gradient Descent

The parameters $\mathbf{w}$ of the logistic regression model are typically learned using optimization techniques such as gradient descent. 

#### Gradient Descent Algorithm

1. Initialize the weight vector $\mathbf{w}$ and the bias term $b$.
2. Compute the gradient of the loss function with respect to the parameters.
3. Update the parameters in the direction opposite to the gradient to minimize the loss.
4. Repeat steps 2 and 3 until convergence or a predefined number of iterations.

The objective is to minimize a loss function, such as the cross-entropy loss, which measures the difference between the predicted probabilities and the actual labels.

## Advantages and Disadvantages

### Advantages

1. **Simple and Interpretable**: Logistic regression provides interpretable results, with coefficients indicating the strength and direction of the relationships between input features and the outcome.
2. **Efficient for Binary Classification**: Logistic regression is computationally efficient and well-suited for binary classification tasks.
3. **Regularization**: It can be extended with regularization techniques to prevent overfitting and improve generalization performance.

### Disadvantages

1. **Assumes Linearity**: Logistic regression assumes a linear relationship between input features and the log odds of the outcome. It may not perform well if the true relationship is highly non-linear.
2. **Limited Expressiveness**: Logistic regression cannot capture complex interactions between features.
3. **Sensitive to Outliers**: Outliers in the data can disproportionately influence the estimated coefficients and affect the model's performance.

## Applications

1. **Medical Diagnosis**: Logistic regression is widely used in medical research for predicting the likelihood of disease based on patient characteristics.
2. **Credit Scoring**: It is used in the banking and finance industry for assessing credit risk and determining loan approvals.
3. **Marketing Analytics**: Logistic regression is employed in marketing analytics for predicting customer churn and targeting marketing campaigns.

![Logistic Regression](https://upload.wikimedia.org/wikipedia/commons/c/cb/Exam_pass_logistic_curve.svg) 
image from wikipedia
