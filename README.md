# AIDS Patient Machine Learning Analysis

This repository contains an exploratory data analysis and machine learning project based on a healthcare dataset related to patients diagnosed with AIDS.

The project investigates clinical and categorical patient information, performs preprocessing and feature analysis, addresses class imbalance, and compares different machine learning models for binary classification.

> This project is intended for educational and portfolio purposes only. It is not intended to provide medical advice, diagnosis, or clinical decision support.

---

## Dataset Overview

The dataset used in this project contains healthcare statistics and categorical information about patients who have been diagnosed with AIDS.

It includes clinical measurements, demographic information, treatment-related variables, and binary/categorical indicators describing patient conditions and treatment history.

The target variable is:

- `infected`: binary classification target. The patient is infected with AIDS (0=No, 1=Yes)

The dataset was obtained from Kaggle and is related to a clinical study/article concerning AIDS patient treatment and outcomes.

- Dataset source: [Kaggle - AIDS Virus Infection Prediction](https://www.kaggle.com/datasets/aadarshvelu/aids-virus-infection-prediction/data)
- Related article/reference: [A trial comparing nucleoside monotherapy with combination therapy in HIV-infected adults with CD4 cell counts from 200 to 500 per cubic millimeter.](10.1056/NEJM199610103351501)

For licensing and privacy reasons, the dataset is not included in this repository.  
Please download it directly from Kaggle before running the notebook.

---

## Attribute Information

The dataset contains the following attributes:

| Attribute | Description |
|---|---|
| `time` | TODO: add description |
| `trt` | TODO: add description |
| `age` | TODO: add description |
| `wtkg` | TODO: add description |
| `hemo` | TODO: add description |
| `homo` | TODO: add description |
| `drugs` | TODO: add description |
| `karnof` | TODO: add description |
| `oprior` | TODO: add description |
| `z30` | TODO: add description |
| `zprior` | TODO: add description |
| `preanti` | TODO: add description |
| `race` | TODO: add description |
| `gender` | TODO: add description |
| `str2` | TODO: add description |
| `strat` | TODO: add description |
| `symptom` | TODO: add description |
| `treat` | TODO: add description |
| `offtrt` | TODO: add description |
| `cd40` | TODO: add description |
| `cd420` | TODO: add description |
| `cd80` | TODO: add description |
| `cd820` | TODO: add description |
| `infected` | Target variable for binary classification. |

---

## Project Goals

The main goals of this project are:

- explore the structure and characteristics of the AIDS healthcare dataset;
- analyze numerical and categorical features;
- inspect class distribution and possible imbalance;
- visualize feature distributions and correlations;
- preprocess the dataset for machine learning;
- handle class imbalance through oversampling;
- compare multiple classification algorithms;
- evaluate model performance using cross-validation and test-set metrics.

---

## Methodology

The project follows these main steps:

1. Dataset loading and inspection
2. Exploratory Data Analysis
3. Missing value analysis
4. Feature type identification
5. Categorical feature encoding
6. Outlier analysis
7. Correlation analysis
8. Feature importance analysis
9. Class imbalance handling
10. Model training and comparison
11. Hyperparameter tuning
12. Final evaluation

---

## Class Imbalance Handling

The target classes were imbalanced in the original dataset.  
To address this issue, Random Oversampling was applied to the minority class.

| Dataset version | Class 0 | Class 1 |
|---|---:|---:|
| Original dataset | TODO | TODO |
| After oversampling | TODO | TODO |

---

## Machine Learning Models

The following classification models were tested:

- Random Forest
- Decision Tree
- Support Vector Classifier
- Logistic Regression
- K-Nearest Neighbors
- Multi-Layer Perceptron

The models were evaluated using cross-validation and final test-set evaluation.

---

## Results

The models were compared using accuracy, classification reports, confusion matrices, and learning curves.

| Model | Mean CV Accuracy | Test Accuracy |
|---|---:|---:|
| Random Forest | TODO | TODO |
| Decision Tree | TODO | TODO |
| SVC | TODO | TODO |
| Logistic Regression | TODO | TODO |
| K-Nearest Neighbors | TODO | TODO |
| MLP Classifier | TODO | TODO |

The best-performing model was:

```text
TODO: insert best model
