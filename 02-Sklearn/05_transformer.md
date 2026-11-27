## Transformers

### What is a Transformer?

A Transformer is an object in scikit-learn that changes or prepares data into a suitable format for machine learning model.

<hr>

### Why do we need Transformers?

We use transformers to:
- Scale numerical values.
- Convert text categories into numbers.
- Handle missing values.
- Create new features.
- Reduce the number of features.

<hr>

### Types of Transfromers

#### 1. Scalling Transformers
Used to bring numerical features into a suitable scale.

Examples:
- ```StandardScaler```
- ```MinMaxScaler```
- ```RobustScaler``` etc.

#### 2. Encoding Transformers
Used to convert categorical data into numerical values.

Examples:
- ```OneHotEncoder```
- ```OridinalEncoder```
- ```LabelEncoder``` etc.

#### 3. Missing Value Tranformers
Used to fill missing values in datasets.

Example:
- ```SimpleImputer```
- ```KNNImputer```

#### 4. Feature Engineering Transformers
Used to create new features or modify existing features.

Example:
- ```PolynomialFeatures```
- ```FunctionTransfer```
- ```Binarizer```

#### 5. Dimensionality Reduction Transformers
Used to reduce the number of features in a dataset.

Example:
- ```PCA```
- ```TruncatedSVD```
- ```VarianceThreshold```