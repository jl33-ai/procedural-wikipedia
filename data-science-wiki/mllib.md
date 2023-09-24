# Machine Learning with MLlib 🚀
### Created by @jl33-ai 👦🏻

Apache Spark MLlib is a machine learning library. It provides multiple types of machine learning algorithms, including classification, regression, clustering, and collaborative filtering, as well as tools for model selection and evaluation, and pipelines for constructing, evaluating, and tuning ML workflows.

## Installation 🔧
Before you start with MLlib, you need to have Apache Spark installed on your machine. You can download it [here](https://spark.apache.org/downloads.html).
For installing MLlib, use the following command:
```bash
pip install pyspark
```

## Features 🌟

- **Data Preparation:** Data handling utilities for pre-processing data. It has tools for feature transformation, for example Normalizer, StandardScaler, etc.

- **Algorithms:** Common learning algorithms such as classification, regression, clustering, and collaborative filtering.

- **Utilities:** Linear algebra, statistics and data handling functions. 

- **Pipelines:** Tools for constructing, evaluating, and tuning ML workflows. 

## Basic Usage 🚴‍♂️ 

Here is a simple example that shows how to train a linear regression model using MLlib.

```python
from pyspark.ml.regression import LinearRegression
from pyspark.sql import SparkSession

# Setup Spark Session
spark = SparkSession.builder.appName('linear_regression_model').getOrCreate()

# Load Data
df = spark.read.csv("data.csv",inferSchema=True,header=True)

# Instantiate Linear Regression
lr = LinearRegression(featuresCol='features', labelCol='label', predictionCol='prediction')

# Fit Model
lr_model = lr.fit(df)

# Print coefficients and intercept
print("Coefficients: " + str(lr_model.coefficients))
print("Intercept: " + str(lr_model.intercept))
```

For more complex examples and tutorials, please refer to the [official documentation](https://spark.apache.org/docs/latest/ml-guide.html).

## License 📄
Apache Spark and Spark MLlib are open source projects under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).

## Contributions 🤝
Contributions are highly appreciated. Before contributing, please make sure to read the contributing guide in the [Apache Spark website](https://spark.apache.org/contributing.html).