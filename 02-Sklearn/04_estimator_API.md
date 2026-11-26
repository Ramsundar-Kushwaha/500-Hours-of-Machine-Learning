## Estimator API

Scikit-Learn follows a consistent API. most estimators follow this general patterns

Example:<br>
```
# 1. import module
from sklearn.linear_model import LinearRegression

# 2. instantiate
model = LinearRegression()

# 3. fit
model.fit(X_train, Y_train)

# 4. predict
predictions = model.predict(X_test)

# 5. evaluate
score = model.score(X_test, Y_test)
```

<hr>

```fit()```<br>
*Learns from data*<br>
*Commonly used by all estimators*

```predict()```<br>
*Generate predictions*<br>
*Commonly used by  predictors*

```transform()```<br>
*Transform data*<br>
*Commonly used by transformers*

```fit_transform()```<br>
*Fit and transform*<br>
*Commonly used by transformers*

```score()```<br>
*Evaluate performance*<br>
*Used by many predictors*

```get_params()```<br>
*Retrieve configuration*<br>
*Commonly used by Estimators*

```set_params()```<br>
*Modify configuration*<br>
*Commonly used by Estimators*

<hr>

### Parameters vs Learned Attributes

```
from sklearn.linear_model import LinearRegression
model = LinearRegression()

# Before training, you can inspect its parameters
print(model.get_params())

model.fit(X_train, Y_train)

# After training, the model learned the attributes
print(model.coef_)
print(model.intercept_)
```
#### Parameters (Hyperparemeters)
*I. Parameters configured before fitting.*<br>
*II. Controlls model behaviour.*<br>
*III. ```max_iter, c, max_depth, learning_rate``` etc.*<br>
*IV. it is also called as Hyperparameters.*

#### Learned attributes
*I. Obtained during fitting.*<br>
*II. Represent learned information*<br>
*III. ```coef_, intercept_, classes_```*

The training underscore convention (```-```) is used for many attributes learned during fitting.

<hr>

### Estimator tags and inspection

Scikit-Learn also provide mechanism for inspecting estimator capabilities and requirements.

For example:<br>
```
from sklearn.base import is_classifier, is_regressor
from sklearn.linear_model import LogisticRegression, LinearRegression

classifier = LogisticRegression()
regressior = LinearRegression()

print(is_classifier(classifier)) # True
print(is_regressor(regression)) # True

# check whether an estimator has a particular method
print(hasattr(classifier, "predict_proba"))
```

<hr>

### Estimator Cloning
