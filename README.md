# Predicting Student Dropout Risk in Online Learning Using a Stacked Ensemble Machine Learning Model

Honours research project, BSc Honours in Computer Science, University of Limpopo.

## What this project does
It predicts which students in an online course are at risk of dropping out, using their click activity on the learning platform.

## Data
KDD Cup 2015 MOOC dataset: 29.2 million clickstream events, combined into one record for each of 157,943 students. The notebook downloads the dataset from Kaggle (samyakjhaveri/mooc-final).

## Method
- Selected 22 of 25 features using Pearson correlation, the ANOVA F-test and Mutual Information
- Handled class imbalance with random undersampling
- Split the data 80/20 with stratification and scaled the features using the training data only
- Trained Logistic Regression, Random Forest, XGBoost and a stacked ensemble

## Results
| Model | ROC AUC |
|---|---|
| XGBoost | 84.86% |
| Stacked ensemble | 84.80% |
| Random Forest | 83.72% |
| Logistic Regression | 83.02% |

SHAP analysis showed that the number of active days was the strongest predictor of dropout.

## How to run
1. Open the notebook in Google Colab.
2. Add your Kaggle API token as a Colab secret named KAGGLE_API_TOKEN.
3. Run all cells.

## Author
Thabisile Moloi - https://thabisilemoloi.github.io/
