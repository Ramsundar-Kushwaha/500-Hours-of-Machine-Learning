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

here,<br>
*```fit()``` - calculates the mean and standard deviation of the traning data.*<br>
*```transform()``` - uses those learned values to standardize the data.*

You can also combine both operation using:
```x_scaled = Scaler.fit_transform(x)```

**Important:** ```fit_transform()``` is a convenient combination of ```fit()``` and ```transform()```. It is commonly used for training data preprocessing.