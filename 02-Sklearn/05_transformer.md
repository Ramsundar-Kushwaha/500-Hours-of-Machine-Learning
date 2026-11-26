## Transformers

### What is a Transformer?

A Transformer is an object in scikit-learn that changes or prepares data into a suitable format for machine learning model.

### Why do we need Transformers?

We use transformers to:<br>
*I. Scale numerical values.*<br>
*II. Convert text categories into numbers.*<br>
*III. Handle missing values.*<br>
*IV. Create new features.*<br>
*V. Reduce the number of features.*

### Types of Transfromers

#### 1. Scalling Transformers
*Used to bring numerical features into a suitable scale.*

Examples:<br>
*```StandardScaler```*<br>
*```MinMaxScaler```*<br>
*```RobustScaler``` etc.*

#### 2. Encoding Transformers
*Used to convert categorical data into numerical values.*

Examples:<br>
*```OneHotEncoder```*<br>
*```OridinalEncoder```*<br>
*```LabelEncoder``` etc.*

#### 3. Missing Value Tranformers
*Used to fill missing values in datasets.*

Example:<br>
*```SimpleImputer```*<br>
*```KNNImputer```*

#### 4. Feature Engineering Transformers
*Used to create new features or modify existing features.*

Example:<br>
*```PolynomialFeatures```*<br>
*```FunctionTransfer```*<br>
*```Binarizer```*

#### 5. Dimensionality Reduction Transformers
*Used to reduce the number of features in a dataset.*

Example:<br>
*```PCA```*<br>
*```TruncatedSVD```*<br>
*```VarianceThreshold```*