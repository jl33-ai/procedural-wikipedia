# Model Interpretability and Explainability: SHAP and LIME 🧠
#### Created by @jl33-ai 👦🏻

## Table of Contents 📚
- [Introduction](#introduction)
- [SHAP](#shap)
- [LIME](#lime)
- [Examples](#examples)
- [Conclusion](#conclusion)

<a name="introduction"></a>
## Introduction 📖
Model Interpretability and Explainability are two essential aspects of modern machine learning. They leverage crucial insights on model predictions, resulting in greater trust and understanding of these models. In this notebook, we focus on two popular concepts, SHAP and LIME.

- `SHAP (SHapley Additive exPlanations)`: It's a unified measure of feature importance that allocates each feature an importance value for a particular prediction.
- `LIME (Local Interpretable Model-Agnostic Explanations)`: It's a technique that explains the predictions of any classifier in an interpretable and faithful manner.

<a name="shap"></a>
## SHAP 🔍
SHAP connects game theory with local explanations. The SHAP value interpretation considers the contribution of a feature value to a prediction as compared to the prediction made by some baseline.

Features:
- Fast exact computation for tree ensemble methods.
- Connects optimal credit allocation with unique and local explanations.

<a name="lime"></a>
## LIME 📝
LIME provides local model interpretability by fitting a simpler model (like linear regression) around the prediction to learn what the underlying model is doing in that space.

Features:
- It's model-agnostic, suitable for any machine learning model.
- It provides reliable local fidelity by giving explanations which work in localized regions.

<a name="examples"></a>
## Examples 📚

```python
# Example: Using SHAP on XGBoost model
import shap
import xgboost

# train XGBoost model
X,y = shap.datasets.boston()
model = xgboost.train({"learning_rate": 0.01}, xgboost.DMatrix(X, label=y), 100)

# explain the model's predictions using SHAP
explainer = shap.TreeExplainer(model)
shap_values = explainer.shap_values(X)

# visualize the first prediction's explanation
shap.force_plot(explainer.expected_value, shap_values[0,:], X.iloc[0,:])

# Example: Using LIME on Random Forest Classifier
import lime
import lime.lime_tabular
from sklearn.ensemble import RandomForestClassifier

rf = RandomForestClassifier(n_estimators = 100)
rf.fit(X_train, y_train)

explainer = lime.lime_tabular.LimeTabularExplainer(X_train)
exp = explainer.explain_instance(X_test[0], rf.predict_proba)

# Visualizing the explanation
exp.show_in_notebook()
```

<a name="conclusion"></a>
## Conclusion 🎯
Both SHAP and LIME provide different ways to interpret and explain model predictions. Understanding these can foster increased confidence in a model's decisions, which is vital in critical-impact areas like healthcare, finance, and many more.