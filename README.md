# ML Excercise - E-commerce Company 🌐

## Overview
This repository contains the solution to a practical machine learning exercise using a product dataset from Mercado Libre Argentina (MLA). The objective is to preprocess the product listing dataset, perform an exploratory data analysis (EDA) and train a machine learning model to predict whether a product is new or used (condition). 


## Dataset
The dataset, titled **MLA\_100k.jsonlines**, contains 100,000 product listings from Mercado Libre Argentina, each with 48 features. The main objective is to predict the **condition** of a product—whether it is *new* or *used*. Key features include **price**, **accepts\_mercadopago**, **listing\_type\_id**, **free\_shipping**, **local\_pick\_up**, **mode**, **initial\_quantity**, **available\_quantity**, **status**, **automatic\_relist**, and **buying\_mode**. The data is stored in **JSON Lines format**, with several fields organized as nested structures (e.g., the **shipping** field).

## Installation And Setup

1. clone the repository.
```
git clone https://github.com/KevinMG1601/ml_exercise.git
```
2. Installing the dependencies.
```
pip install -r requirements.txt 
``` 
3. Run the notebooks, first the one for EDA and then the one for training the model.

## Results
Six classification models were evaluated: Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbors (KNN), Gradient Boosting and XGBoost. The objective was to predict whether a product is new or used.

The following metrics were used to compare the performance of each model:
* **Accuracy:** measures the total proportion of correct predictions.
* **Precision:** indicates how accurate the positive predictions are (used products).
* **Recall:** shows how many used products were correctly identified.
* **F1-Score:** balances precision and recall in a single metric.
* **ROC-AUC:** evaluates the overall ability of the model to distinguish between classes.

| Modelo              | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---------------------|----------|-----------|--------|----------|---------|
| **XGBoost**         | **0.8300** | 0.8059   | **0.8353** | **0.8203** | **0.8303** |
| Gradient Boosting   | 0.8212   | **0.8097** | 0.8041 | 0.8069   | 0.8200  |
| Random Forest       | 0.8212   | 0.7762   | 0.8643 | 0.8179   | 0.8240  |
| Decision Tree       | 0.8191   | 0.7778   | 0.8549 | 0.8145   | 0.8215  |
| KNN                 | 0.8064   | 0.7820   | 0.8088 | 0.7952   | 0.8066  |
| Logistic Regression | 0.7335   | 0.9038   | 0.4771 | 0.6245   | 0.7165  |


## Conclusion 
After training and evaluating multiple classification algorithms — including Logistic Regression, Decision Tree, Random Forest, KNN, Gradient Boosting, and XGBoost — it was determined that XGBoost is the most effective model for predicting whether a product is new or used.

The XGBoost model achieved the following results on the test set:

* Accuracy: 83.00%.
* Accuracy: 80.59
* Recall: 83.53
* F1-Score: 82.03%.

This represents the best balance between accuracy (avoiding false positives) and recall (detecting the most used products), achieving the highest F1-Score among all models evaluated. Its ability to handle non-linear relationships and avoid over-fitting thanks to regularization makes it a solid and robust option for this problem.
