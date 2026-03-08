# K-Nearest Neighbors (KNN) – Classification and Regression

## Overview

K-Nearest Neighbors (KNN) is a supervised machine learning algorithm used for both classification and regression tasks. It is a instance-based learning method that makes predictions based on the similarity between data points.

Instead of learning an explicit model during training, KNN stores the training data and predicts the output for new data points by analyzing the nearest neighbors in the feature space.

---

## Key Concepts

### 1. Nearest Neighbors

The algorithm identifies the K closest data points in the training dataset to a new data point.

### 2. Value of K

K represents the number of neighbors considered for making predictions. The choice of K affects the model’s performance.

* Small K may lead to overfitting.
* Large K may lead to underfitting.

### 3. Distance Metric

KNN uses distance measures to determine similarity between points. Common distance metrics include:

* Euclidean Distance
* Manhattan Distance

---

## KNN for Classification

In classification problems, the algorithm assigns the class label based on the majority class among the K nearest neighbors.

### Example

If K = 5 and among the nearest neighbors:

* 3 belong to Class A
* 2 belong to Class B

The predicted class will be **Class A**.

---

## KNN for Regression

In regression problems, the algorithm predicts a continuous value by taking the average of the target values of the K nearest neighbors.

### Example

If K = 3 and the nearest neighbors have values:

* 200
* 220
* 210

The predicted value will be the average:

210

---

## Algorithm Steps

1. Choose the number of neighbors K.
2. Calculate the distance between the new data point and all points in the training dataset.
3. Sort the distances and select the K nearest neighbors.
4. For classification, determine the majority class among the neighbors.
5. For regression, compute the average of the neighbor values.
6. Assign the predicted output.

---

## Importance of Feature Scaling

Since KNN relies on distance calculations, features with larger scales can dominate the distance metric. Therefore, feature scaling is essential.

Common scaling techniques include:

* Standardization (StandardScaler)
* Normalization (MinMaxScaler)

---

## Hyperparameters

Important hyperparameters for KNN include:

* **n_neighbors**: Number of neighbors used for prediction
* **metric**: Distance metric used to compute distances
* **weights**: Uniform or distance-based weighting
* **algorithm**: Method used for nearest neighbor search

---

## Advantages

* Simple and intuitive algorithm
* No explicit training phase
* Works well with small datasets
* Effective for multi-class classification problems

---

## Limitations

* Computationally expensive for large datasets
* Sensitive to irrelevant features
* Requires proper feature scaling
* Performance decreases in high-dimensional datasets

---

## Applications

KNN is widely used in several practical applications:

* Image classification
* Recommendation systems
* Pattern recognition
* Medical diagnosis
* Fraud detection

---

## Implementation

The implementation in this project uses the Scikit-learn library to demonstrate both classification and regression using the KNN algorithm.

Typical workflow:

1. Load dataset
2. Perform feature scaling
3. Split data into training and testing sets
4. Train KNN model
5. Evaluate model performance

---

## Evaluation Metrics

For classification tasks:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

For regression tasks:

* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)
* R-squared Score

---

## Conclusion

K-Nearest Neighbors is a simple yet powerful algorithm for solving both classification and regression problems. Although computationally expensive for large datasets, it remains an important foundational algorithm for understanding distance-based learning methods in machine learning.
