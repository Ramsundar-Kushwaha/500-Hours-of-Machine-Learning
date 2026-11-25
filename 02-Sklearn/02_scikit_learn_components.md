## Components of Scikit-Learn

### 1. Estimators:

*I. An Estimator is an object that learn from data.*<br>
*II. In simple words, an Estimator is an object that provides a ```fit()``` method to learn patterns or parameters from training data.*<br>

For example:

```
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_train, Y_train)
```

Here,<br>
*LinearRegression is the estimator class.*<br>
*model is an estimator object (an instance of that class)*<br>
*The ```fit()``` methods learns model parameters from the training data.*

**Important:** Estimators are not limited to predictive models, preprocessing object, such as StandardScalar, are also an estimators.

<hr>

### 2. Transformers

*I. A Transfromer is an object that learns how to transform data and then applies that transformation.*

It generally provide two important method:

*1. ```fit()``` - learns the required transformation parameters.*<br>
*2. ```transform()``` - applies the learned transformation to data.*

For example:

```
from sklearn.preprocessing import StandardScalar

Scaler = StandardSaclar()

x = [[1000], [2000], [3000], [4000]]

# learn mean and standard deviation
Scaler.fit(x)

x_scaled = Scaler.transform(x)

print(x_scaled)
```

Here,<br>
*```fit()``` - calculates the mean and standard deviation of the traning data.*<br>
*```transform()``` - uses those learned values to standardize the data.*

You can also combine both operation using:
```x_scaled = Scaler.fit_transform(x)```

**Important:** ```fit_transform()``` is a convenient combination of ```fit()``` and ```transform()```. It is commonly used for training data preprocessing.

<hr>

### 3. Predictors

*I. A Predictor is an estimator that can make prediction using ```predict()``` method.*<br>

For example:

```
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_train, Y_train)

prediction = model.predict(X_test)
```

Here,<br>
*```fit()``` trains the model.*
*```predict()``` generate predictions from new input data.*

For regression, predictions are numerical values.<br>
For classification, predictions are class labels.

Some classifiers also provides:<br>
```model.predict_proba(X_test)```

This returns predicted class probabilities when supported by the estimator.

<hr>

### 4. Model Selection

*I. Model Selection provides tools to split datasets, compare models and find suitable hyperparameters.*<br>

Important functions and classes includes:

*```train_test_split()``` - Split data into training and testing sets.*<br>
*```cross_val_score()``` - Evaluate a model using cross-validation.*<br>
*```GridSearchCV``` - Search through specified hyperparameter combinations.*<br>
*```RandomizedSearchCV``` - Search through sampled hyperparameter combinations.*<br>
*```StratifiedKfold``` - Maintain class proportions across folds.*

Example:

```
from sklearn.model_selection import train_test_split

X_train, X_test, Y_train, Y_test = train_test_split(x, y, test_size = 0.2, random_state=42)
```

this devides the dataset into:<br>
*80% training data*<br>
*20% testing data*

<hr>

### 5. Metrices

*I. Metrices help us understand how well a machine learning model performs.*<br>
*II. Scikit-Learn provides different metrices for regression, classificaton and clustering.*

Example:

*Regression: MAE, MSE, RMSE, R^2*<br>
*Classification: Accuracy, Precision-Recall, F1-Score*<br>
*Clustering: Silhoutte Score, Adjusted Rand Index*

Example:
```
from sklearn.metrics import mean_squared_error

mse = mean_squared_error(Y_test, predictions)

print(mse)
```

The metric calculate mse between actual and predicted value.

<hr>

### 6. Pipelines

*I. A Pipeline combines multiple machine learning operations into one workflow*<br>

suppose you want to:<br>
*1. Standardize your data.*<br>
*2. Train a Logistic Regression Model.*<br>
*3. Make predictions*

without a pipeline, you would manually execute each step.

with pipeline:<br>
```
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression

# pipeline - combining StandardScalar and model training
pipeline = Pipeline([('scaler', StandardScaler()), ('model', LogisticRegression())])

pipeline.fit(X_train, Y_train)

predictions = pipeline.predict(x_test)
```

*II. Scikit-Learn automatically performs the preprocessing and model training in the correct order.*<br>
*III. Pipelines are especially important for preventing data leakage when combined with cross-validation.*

<hr>

### 7. Datasets

*I. Scikit-Learn provides built-in datasets for learning and experimentation.*<br>

Some examples:

*1. Iris : Classification*<br>
*2. Breast Cancer: Binary Classification*<br>
*3. wine: Multiclass Classification*<br>
*4. Diabetes: Regression*<br>
*5. Digits: Image Classification*

For example:<br>
```
from sklearn.datasets import load_iris

data = load_iris()

X = data.data
Y = data.target
```

You can use these datasets to proctive machine learning without searching for external datasets.