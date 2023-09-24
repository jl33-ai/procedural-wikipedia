**Created by @jl33-ai 👦🏻**

Evaluation metrics are a key part of any data science project. They allow us to assess the performance of our model, comparing it to previous iterations and potentially other models, helping us fine tune and optimize it based on clearly defined measures.

## Table of Contents 
1. [Confusion Matrix](#Confusion-Matrix)
2. [Accuracy](#Accuracy)
3. [Precision](#Precision) 
4. [Recall](#Recall)
5. [F1 Score](#F1-Score)
6. [Area Under ROC Curve (AUC-ROC)](#AUC-ROC)
7. [Log Loss](#Log-Loss)
8. [Mean Absolute Error (MAE)](#MAE)
9. [Mean Squared Error (MSE)](#MSE)
10. [R Squared (R²)](#R²)

   
## Confusion Matrix 
A confusion matrix is a table layout that allows visualization of the performance of an algorithm.

- True Positives (TP): These are cases in which we predicted yes, and the actual is also yes.
- True Negatives (TN): We predicted no, and the actual is also no.
- False Positives (FP): We predicted yes, but the actual is no. (Type I error)
- False Negatives (FN): We predicted no, but the actual is yes. (Type II error)

Example: Detecting spam emails

## Accuracy 
Accuracy speaks to the overall correctness of the classifier.
```markdown
Accuracy = (TP+TN) / (TP+FP+FN+TN)
```
Example: Detecting spam emails (assuming balanced classes)

## Precision 
Precision talks about how precise/accurate your model is out of those predicted positive, how many of them are actual positive.
```markdown
Precision = TP / (TP+FP)
```
Example: If the costs of False Positive is high (e.g., Email spam detection. Because FP is classifying 'Not Spam' as 'Spam') 

## Recall 
Recall actually calculates how many of the Actual Positives our model capture through labeling it as Positive.
```markdown
Recall = TP / (TP+FN)
```
Example: If cost of missing a positive instance is high (e.g., Disease detection) 

## F1-Score 
F1 Score is needed when you want to seek a balance between Precision and Recall.
```markdown
F1 Score = 2*(Recall * Precision) / (Recall + Precision)
```
Example: Where both False Negatives and False Positives are crucial.

## AUC-ROC 📈
AUC - ROC curve is a performance measurement for the classification problems at various threshold settings.
- AUC: Area Under the ROC Curve
- ROC: Receiver Operating Characteristic curve
Example: Evaluating performance across different classification thresholds 

## Log-Loss
Log Loss quantifies the accuracy of a classifier by penalising false classifications.
Lower log-loss means better predictions. 
```markdown
Log Loss = -(1/n) * Σ [y log(p) + (1-y)log(1-p)]
```
Example: In case of multiple categories outputs.

## MAE
Mean Absolute Error (MAE) measures the average magnitude of the errors in a set of predictions, without considering their direction.
```markdown
MAE = 1/n * Σ |y - ŷ|
```
Example: Where we need an understandable measure on the average.

## MSE
Mean Squared Error (MSE) takes the distances from the points to the regression line (these distances are the "errors") and squares them to eliminate any negatives.
```markdown
MSE = 1/n * Σ (y - ŷ)²
```
Example: When larger errors are particularly undesirable.

## R² 
R², also known as the coefficient of determination, is a statistical measure in regression models that determines the proportion of variance in the dependent variable that can be explained by the independent variable. Value between 0 and 1.
```markdown
R² = 1 - (RSS/TSS)
```