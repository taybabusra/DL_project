# DL_project

### Exploratory Data Analysis (EDA)

It is an approach to analyzing and visualizing data sets to summarize their main characteristics, often with the help of statistical graphics and other data visualization methods. The primary goal of EDA is to uncover patterns, relationships, anomalies, and trends in the data, providing insights that can guide further analysis or decision-making processes.

Types of Exploratory Data Analysis

-- There are three main types of EDA:

* Univariate 
* Bivariate 
* Multivariate
  
## Step of project

The following topics were covered in this project:

* Splitting a dataset into training, validation & test sets
* Filling/imputing missing values in numeric columns
* Scaling numeric features to a (0,1) range
* Encoding categorical columns as one-hot vectors
* Training and interpreting model
* Overfitting & hyperparameter tuning
* Making predictions on test
* Saving model on disk
## ANN Model:
1. Normalization: It can be used when data does contain outliers. Scikit-Learn provides a transformer called MinMaxScaler for this. It has a feature_range hyperparameter that lets you change the range if, for some 
reason, you don’t want 0–1 (e.g., neural networks work best with zero-mean inputs, so a range of –1 to 1 is preferable).
2. Standardization: Unlike min-max scaling, standardization does not restrict values to a specific range. However, standardization is much less affected by outliers. 
3. Data with a heavy tail: When a feature’s distribution has a heavy tail (i.e. when values far from the mean are not exponentially rare), both min-max scaling and standardization will squash most values into a small 
range. Models generally don’t like this at all. So before you scale the feature, you should first transform it to shrink the heavy tail, and if possible to make the distribution roughly symmetrical. For example, a 
common way to do this for positive features with a heavy tail to the right is to replace the feature with its square root (or raise the feature to a power between 0 and 1). If the feature has a really long and heavy tail, such as a power law distribution,
then replacing the feature with its logarithm may help. Another approach to handle heavy-tailed features consists in bucketizing the feature. This means chopping its distribution into roughly equal-sized buckets, and replacing each feature value with the index of the bucket it belongs to.
4. Data with multiple peaks: When a feature has a multimodal distribution (i.e., with two or more clear peaks, called modes), it can also be helpful to bucketize it, but this time treating the bucket IDs as categories,
rather than as numerical values. This means that the bucket indices must be encoded, for example using a OneHotEncoder (so you usually don’t want to use too many buckets). This approach will allow the model to more
easily learn different rules for different ranges of this feature value. Another approach to transforming multimodal distributions is to add a feature for each of the modes (at least the main ones). The similarity
measure is typically computed using a radial basis function (RBF)—any function that depends only on the distance between the input value and a fixed point. The most commonly used RBF is the Gaussian RBF, whose output
value decays exponentially as the input value moves away from the fixed point.

## Summary of RNNs, LSTMs, GRUs, and deep RNNs in one line each:

* Recurrent Neural Networks (RNNs): Basic neural network architecture with connections between units forming directed cycles, suitable for sequential data processing.
* Long Short-Term Memory (LSTM) Networks: RNN architecture with specialized memory cells and gating mechanisms to capture long-term dependencies more effectively.
* Gated Recurrent Units (GRUs): Simplified RNN variant with fewer parameters than LSTMs, featuring update and reset gates to control information flow.
* Deep Recurrent Neural Networks (RNNs): Extension of RNN architecture with multiple recurrent layers stacked hierarchically, allowing for learning complex hierarchical representations of sequential data.


## Support Vector Machine Terminology

* Hyperplane: Hyperplane is the decision boundary that is used to separate the data points of different classes in a feature space. In the case of linear classifications, it will be a linear equation i.e. wx+b = 0.
* Support Vectors: Support vectors are the closest data points to the hyperplane, which plays a critical role in deciding the hyperplane and margin. 
* Margin: Margin is the distance between the support vector and hyperplane. The main objective of the support vector machine algorithm is to maximize the margin.  The wider margin indicates better classification performance.
* Kernel: Kernel is the mathematical function, which is used in SVM to map the original input data points into high-dimensional feature spaces, so, that the hyperplane can be easily found out even if the data points are not linearly separable in the original input space. Some of the common kernel functions are linear, polynomial, radial basis function(RBF), and sigmoid.
* Hard Margin: The maximum-margin hyperplane or the hard margin hyperplane is a hyperplane that properly separates the data points of different categories without any misclassifications.
* Soft Margin: When the data is not perfectly separable or contains outliers, SVM permits a soft margin technique. Each data point has a slack variable introduced by the soft-margin SVM formulation, which softens the strict margin requirement and permits certain misclassifications or violations. It discovers a compromise between increasing the margin and reducing violations.
* C: Margin maximization and misclassification fines are balanced by the regularisation parameter C in SVM. The penalty for going over the margin or misclassifying data items is decided by it. A stricter penalty is imposed with a greater value of C, which results in a smaller margin and perhaps fewer misclassifications.
* Hinge Loss: A typical loss function in SVMs is hinge loss. It punishes incorrect classifications or margin violations. The objective function in SVM is frequently formed by combining it with the regularisation term.
* Dual Problem: A dual Problem of the optimization problem that requires locating the Lagrange multipliers related to the support vectors can be used to solve SVM. The dual formulation enables the use of kernel tricks and more effective computing.
