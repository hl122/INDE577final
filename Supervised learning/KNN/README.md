# K-Nearest Neighbors (KNN)

This repository showcases the practical implementation and diverse applications of K-Nearest Neighbors.

## File descriptions
Inside "K-Nearest_neighbors.ipynb," you'll find detailed explanations and coding examples demonstrating the utility of K-Nearest Neighbors algorithms.

## Introduction to K-Nearest Neighbors (KNN) Modeling


K-Nearest Neighbors (KNN) is a simple yet powerful supervised machine learning algorithm used for classification and regression tasks. It operates on the principle of similarity, where instances are classified or predicted based on the majority vote or average of their nearest neighbors in the feature space.

## Fundamentals of K-Nearest Neighbors

KNN does not involve explicit model training; instead, it stores the entire training dataset as its "knowledge" and makes predictions based on the similarity between new instances and existing data points. The choice of the number of neighbors (\( K \)) is a crucial parameter in KNN, affecting the model's performance and generalization capabilities.


# Basics of KNN Algorithm

## Distance Metrics in KNN

The choice of distance metric plays a crucial role in KNN, as it determines the notion of similarity between data points. Common distance metrics include Euclidean distance, Manhattan distance, and cosine similarity, each suitable for different types of data and feature spaces.

Euclidean distance formula:

$$
d(\mathbf{p}, \mathbf{q}) = \sqrt{\sum_{i=1}^{n} (p_i - q_i)^2} \
$$

The Euclidean distance between two points in n-dimensional space is the straight-line distance between them, calculated using the Pythagorean theorem. The Euclidean distance captures the "as-the-crow-flies" distance between two points and is influenced by the magnitude of differences in all dimensions. It is commonly used when the data points are continuous and the dimensions are independent of each other.

Manhattan distance formula:

$$
d(\mathbf{p}, \mathbf{q}) = \sum_{i=1}^{n} |p_i - q_i| \
$$

The Manhattan distance, also known as the taxicab or city block distance, measures the distance between two points by summing the absolute differences of their coordinates. The Manhattan distance represents the distance traveled along the grid-like paths of a city, where movements are restricted to horizontal and vertical paths. Unlike the Euclidean distance, the Manhattan distance is less affected by outliers and focuses on the total movement along each dimension independently.

## Choosing the Optimal Value of $K$

Selecting the appropriate value of $K$ is essential for achieving optimal performance in KNN. A small value of $K$ may result in overfitting and sensitivity to noise, while a large value of $K$ may lead to underfitting and increased computational costs. Various techniques, such as cross-validation, can be employed to determine the optimal value of $K$.

## Handling Categorical Features in KNN

KNN inherently supports both numerical and categorical features. When dealing with categorical features, appropriate encoding techniques such as one-hot encoding or label encoding may be required to ensure compatibility with distance-based calculations in KNN.

# Model Evaluation and Parameter Tuning

## Cross-Validation Techniques for KNN

Cross-validation is a robust technique for assessing the generalization performance of KNN models and selecting optimal hyperparameters. Common cross-validation methods, such as k-fold cross-validation and leave-one-out cross-validation, help mitigate issues of overfitting and variance estimation.

![Fitting](https://miro.medium.com/v2/resize:fit:1400/0*jB3VzCwWSwGXUX82.png)
Image from Geetha Mattaparthi

## Performance Metrics for KNN

Evaluation of KNN models involves assessing their predictive performance using suitable performance metrics. For classification tasks, metrics such as accuracy, precision, recall, and F1 score provide insights into the model's classification capabilities. For regression tasks, metrics like mean squared error (MSE) and R-squared are commonly used to evaluate predictive accuracy.

## Tuning Hyperparameters in KNN

Hyperparameter tuning is essential for optimizing the performance of KNN models. Techniques such as grid search and random search can be employed to systematically search the hyperparameter space and identify the optimal combination of hyperparameters, including the value of $K$ and the choice of distance metric.

## Decision Boundary Visulization

Evaluating the accuracy of a KNN model using decision boundary visualization involves plotting the decision boundary in the feature space to visually assess how well the model separates different classes or regions. By visualizing the decision boundary, you can gain insights into the model's performance and identify potential areas for improvement. However, it's essential to remember that decision boundary visualization is primarily a qualitative assessment and may not provide a comprehensive evaluation of the model's accuracy on its own. It should be complemented with quantitative performance metrics and cross-validation techniques for a more robust evaluation.

## Applications of KNN

KNN finds applications across various domains, including:

- **Credit Scoring:** Predicting credit risk by analyzing the similarity between new loan applicants and existing customers.
- **Recommender Systems:** Recommending products or services to users based on the preferences of similar users.
- **Anomaly Detection:** Identifying anomalies or outliers in data by comparing them to the majority of normal instances.
- **Bioinformatics:** Classifying biological data, such as DNA sequences, based on their similarity to known patterns.
- **Image Recognition:** Recognizing patterns in images by comparing them to similar images in the training dataset.

## Advantages and Disadvantages

### Advantages

- **Simplicity:** KNN is easy to understand and implement, making it an accessible choice for beginners and practitioners.
- **Non-Parametric:** KNN makes no assumptions about the underlying data distribution, making it versatile and adaptable to various types of data.
- **Interpretability:** KNN provides transparent decision-making by directly using the nearest neighbors for classification or regression.

### Disadvantages

- **Computational Complexity:** KNN requires storing the entire training dataset and computing distances to all data points during prediction, resulting in high computational costs for large datasets.
- **Sensitivity to Feature Scaling:** KNN is sensitive to the scale of features, where features with larger scales may dominate the distance calculation.
- **Curse of Dimensionality:** In high-dimensional feature spaces, the notion of distance becomes less meaningful, leading to degraded performance and increased computational burden.