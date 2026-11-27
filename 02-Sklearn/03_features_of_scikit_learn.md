## Important Feature of Scikit-Learn

### 1. Consistent API (Application Programming Interface)

- Allmost all Scikit-Learn estimators follow a consistent interface.

For example:
```
model = someAlgorithm()
model = fit(X_train, Y_train)
predictions = model.predict(X_test)
```

You can use almost the same workflow with:
- Linear Regression
- Logistic Regression
- Descision Tree
- Random Forest
- Support Vector Machine

You don't need to learn a completely different training interface for every algorithm.

### 2. Data Preprocessing

- Machine Learning algorithm generally require properly prepared input data.
- Scikit-Learn provides several preprocessing tools.

For example:

- ```StandardScalar``` - Standardization
- ```MinMaxScalar``` - Normalization to a specified range
- ```RobustScalar``` - Scaling using median and interquartile range
- ```LabelEncoder``` - Handle missing values
- ```OneHotEncoder``` - Convert categorical features into binary column
- ```SimpleImputer``` - Handle missing values
- ```PolynomialFeatures``` - Generate polynomial and interaction features

### 3. Support Supervised Learning

- Scikit-Learn support supervised learning algorithms.
- Supervised Learning means training a model using labeled data.

There are two major categories:

#### A. Regression
Used to predict continous numerical values

Example:
- House Price Prediction
- Salary Prediction
- Temperature Prediction

Important Algorithms:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Descision Tree Regression
- Random Forest Regression
- Support Vector Regression

#### B. Classification
Used to predict categories or classes

Example:
- Spam detection
- Disease Classification
- Customer churn prediction

Important Algorithms:
- Logistic Regression
- K-Nearest Neighbours
- Descision Tree Classifiers
- Random Forest Classifiers
- Support Vector Classifiers
- Naive Bayes

<hr>

### 4. Support Unsupervised Learning
- Scikit-Learn also supports unsupervised learning.
- Unsupervised learning means finding patterns or structures in data without labeled target values.

Two important categories:

#### A. Clustering
Groups similar data points together

Some Algorithms:
- K-Means
- DBSCAN
- Agglomerative Clustering
- Mean Shift

Example: Grouping customers based on their behaviour.

#### B. Dimensionality Reduction

I. Reduce the number of features while attempting to preserve useful information.

Some Algorithms:
- PCA (Principal Component Analysis)
- Truncated SVD
- NMF (Non-negative Matrix Factorization)
- t-SNE

Example: Reducing 100 features to 10 features

<hr>

### 5. Model Evaluation

I. Scikit-Learn provides tools to evaluate machine learning models.

Important evaluation function includes:
- confusion_matrix()
- classification_report()
- precision_score()
- recall_score()
- F1_score()

For regression
- mean_absolute_error()
- mean_squared_error()
- r2_score()

Evaluation is important because a model that performs well on trianing data might performs poorly on unseen data.

<hr>

### 6. Cross Validation

- Cross-Validation is a technique used to evaluate how well a model generalizes to unseen data.
- Instead of relying an just one train_test_split, cross-validation evalueates a model across multiple data splits.

Scikit-Learn Provides:
- KFold
- StratifiedKFold
- LeaveOneOut
- cross-val_score()
- cross_validate()

<hr>

### 7. Hyperparameter Tuning

- Hyperparameters are configuration values that we set before training a model.

- Example: learning_rate, epoch etc.

<hr>

### 8. Pipeline Support

They are useful for:
- Automating machine learning workflows.
- Preventing data leakage.
- Reducing repetitive code.
- Making model evaluation and cross-validation easier.
- Creating reusable ML workflows.

<hr>

## Limitations of Scikit-Learn

### 1. Not a full deep learning framework
It is not designed for building complex deep neural networks.

### 2. Limited CPU Support
Its standard estimators primarily operates on CPUs

### 3. Not designed for raw unstructured data
Working directly with large collections of raw images, audios, and videos is not its primarly purpose.

### 4. Distribute training limitations
It is not designed as a distributed large-scale training framework.

### 5. Model deployment is not its primary purpose
You generally use additional tools and frameworks to build production APIs and deployment infrastructure.