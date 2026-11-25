## Important Feature of Scikit-Learn

### 1. Consistent API (Application Programming Interface)

*I. Allmost all Scikit-Learn estimators follow a consistent interface.*

For example:<br>
```
model = someAlgorithm()
model = fit(X_train, Y_train)
predictions = model.predict(X_test)
```

You can use almost the same workflow with:<br>
*Linear Regression*<br>
*Logistic Regression*<br>
*Descision Tree*<br>
*Random Forest*<br>
*Support Vector Machine*

You don't need to learn a completely different training interface for every algorithm.

### 2. Data Preprocessing

*I. Machine Learning algorithm generally require properly prepared input data.*<br>
*II. Scikit-Learn provides several preprocessing tools.*

for example:

*```StandardScalar``` - Standardization*<br>
*```MinMaxScalar``` - Normalization to a specified range*<br>
*```RobustScalar``` - Scaling using median and interquartile range*<br>
*```LabelEncoder``` - Handle missing values*<br>
*```OneHotEncoder``` - Convert categorical features into binary column*<br>
*```SimpleImputer``` - Handle missing values*<br>
*```PolynomialFeatures``` - Generate polynomial and interaction features*

### 3. Support Supervised Learning

*I. Scikit-Learn support supervised learning algorithms.*<br>
*II. Supervised Learning means training a model using labeled data.*<br>

There are two major categories:

#### A. Regression
Used to predict continous numerical values

Example:<br>
*I. House Price Prediction*<br>
*II. Salary Prediction*<br>
*III. Temperature Prediction*

Important Algorithms:<br>
*I. Linear Regression*<br>
*II. Ridge Regression*<br>
*III. Lasso Regression*<br>
*IV. Descision Tree Regression*<br>
*V. Random Forest Regression*<br>
*VI. Support Vector Regression*

#### B. Classification
Used to predict categories or classes

Example:<br>
*I. Spam detection*<br>
*II. Disease Classification*<br>
*III. Customer churn prediction*

Important Algorithms:<br>
*I. Logistic Regression*<br>
*II. K-Nearest Neighbours*<br>
*III. Descision Tree Classifiers*<br>
*Iv. Random Forest Classifiers*<br>
*V. Support Vector Classifiers*<br>
*VI. Naive Bayes*

<hr>

### 4. Support Unsupervised Learning
*I. Scikit-Learn also supports unsupervised learning.*<br>
*II. Unsupervised learning means finding patterns or structures in data without labeled target values.*

Two important categories:

#### A. Clustering
Groups similar data points together

Some Algorithms:<br>
*I. K-Means*<br>
*II. DBSCAN*<br>
*III. Agglomerative Clustering*<br>
*Iv. Mean Shift*

Example: Grouping customers based on their behaviour.

#### B. Dimensionality Reduction

*I. Reduce the number of features while attempting to preserve useful information.*<br>

Some Algorithms:<br>
*I. PCA (Principal Component Analysis)*<br>
*II. Truncated SVD*<br>
*III. NMF (Non-negative Matrix Factorization)*<br>
*IV. t-SNE*

Example: Reducing 100 features to 10 features

<hr>

### 5. Model Evaluation

*I. Scikit-Learn provides tools to evaluate machine learning models.*<br>

Important evaluation function includes:<br>
*I. confusion_matrix()*<br>
*II. classification_report()*<br>
*III. precision_score()*<br>
*IV. recall_score()*<br>
*V. F1_score()*

For regression
*I. mean_absolute_error()*<br>
*II. mean_squared_error()*<br>
*III. r2_score()*

Evaluation is important because a model that performs well on trianing data might performs poorly on unseen data.

<hr>

### 6. Cross Validation

*I. Cross-Validation is a technique used to evaluate how well a model generalizes to unseen data.*<br>
*II. Instead of relying an just one train_test_split, cross-validation evalueates a model across multiple data splits.*

Scikit-Learn Provides:
*I. KFold*<br>
*II. StratifiedKFold*<br>
*III. LeaveOneOut*<br>
*IV. cross-val_score()*<br>
*V. cross_validate()*

<hr>

### 7. Hyperparameter Tuning

Hyperparameters are configuration values that we set before training a model.

Example: learning_rate, epoch etc.

<hr>

### 8. Pipeline Support

They are useful for:<br>
*I. Automating machine learning workflows.*<br>
*II. Preventing data leakage.*<br>
*III. Reducing repetitive code.*<br>
*IV. Making model evaluation and cross-validation easier.*<br>
*V. Creating reusable ML workflows.*