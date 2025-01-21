Feature scalling
Feature scaling is a technique used in data preprocessing to standardize or normalize the range of independent variables or features of data. Here's a simple way to understand it:

Imagine a Classroom with Tall and Short Students Suppose you want to compare students' heights (in meters) and weights (in kilograms). Heights might range from 1.5 to 2 meters, while weights could range from 50 to 100 kilograms. If you don't scale these features, the model might give more importance to weight because its values are numerically larger. Why Does This Matter? Many machine learning algorithms (e.g., gradient descent-based models like logistic regression or distance-based models like k-NN) perform better when features are on a similar scale. If not scaled, large values dominate small values, skewing the model's performance.

Min-Max Scaler

The MinMaxScaler is a scaling technique that transforms the data such that all feature values are scaled to a specific range, usually [0, 1].

The formula for scaling using Min-Max Scaler is:

[ X_{\text{scaled}} = \frac{X - X_{\text{min}}}{X_{\text{max}} - X_{\text{min}}} ]

Where:

(X_{\text{min}}) and (X_{\text{max}}) are the minimum and maximum values of a feature in the training data.
(X) is the original value of the feature.
(X_{\text{scaled}}) is the scaled value.
Key Points:

The scaler learns the minimum and maximum values from the training data during the fit step.
These learned parameters are then applied consistently to both the training and testing datasets during the transform step.
Scaling is important for machine learning models that rely on distance or gradient-based optimization to ensure that features contribute equally to the model.

Mean Normalization

Mean normalization is a feature scaling technique that adjusts the range of the data by centering the features around zero. This is done by subtracting the mean of each feature and dividing by the range or standard deviation. The goal is to standardize the data, ensuring that features with different scales or units contribute equally to the learning process. Rearly used in sklearn and there is no class in sklearn. You have to write a code by own.

Max Absolute Scaling is a feature scaling technique that transforms the data by dividing each feature by its maximum absolute value. This ensures that all features lie within the range [-1,1] while maintaining the sparseness of the data (i.e., the presence of many zeros in datasets like text or recommendation systems). Not used that much. Basically used in sparse data set with many zeros. Sklearn has class called MaxAbsScaler.
