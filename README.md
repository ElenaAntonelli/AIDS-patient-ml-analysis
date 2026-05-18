# AIDS Patient Machine Learning Analysis

This repository contains an exploratory data analysis and machine learning project based on a healthcare dataset related to patients diagnosed with AIDS.

The project investigates clinical and categorical patient information, performs preprocessing and feature analysis, addresses class imbalance, and compares different machine learning models for binary classification.

> This project is intended for educational and portfolio purposes only. It is not intended to provide medical advice, diagnosis, or clinical decision support.

---

## Dataset Overview

The dataset used in this project contains healthcare statistics and categorical information about patients who have been diagnosed with AIDS.

It includes clinical measurements, demographic information, treatment-related variables, and binary/categorical indicators describing patient conditions and treatment history.

The target variable is:

- `infected`: binary classification target. 

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
| `time` | time to failure or censoring. The time in hours/days elapsed until an event of interest (development of advanced symptoms or the achievement of a specific health state) occurs.Or it is the censoring time, i.e. the patient is still under treatment or has not yet reached the event of interest. |
| `trt` | treatment indicator (0 = ZDV; 1 = ZDV + ddI, 2 = ZDV + Zal, 3 = ddI). Where ZDV = zidovudine, ddI = didanosine, Zal = zalcitabine. |
| `age` | age (yrs) at baseline |
| `wtkg` | weight (kg) at baseline |
| `hemo` | hemophilia (0=no, 1=yes) |
| `homo` | homosexual activity (0=no, 1=yes) |
| `drugs` | history of IV drug use (0=no, 1=yes) |
| `karnof` | Karnofsky score (on a scale of 0-100). It is a system used to evaluate the functional status and autonomy of a patient with a disease.The Karnofsky score ranges from 100 to 0, where: 100 represents a perfect state of health and normal activity without signs of illness; 0 represents a state of coma or death. |
| `oprior` | Non-ZDV antiretroviral therapy pre-175 (0=no, 1=yes). So, it evaluates whether the patient has undergone non-zidovudine-based antiretroviral therapy prior to initiating treatment (175 weeks earlier). |
| `z30` | ZDV was administered in the 30 days prior to the 175-week mark of observation. (0=no, 1=yes) |
| `preanti` | days pre-175 antiretroviral therapy. Number of days or the duration that a patient has been on anti-retroviral therapy before reaching the 175-week mark since the start of observation or treatment. |
| `race` | race (0=White, 1=non-white) |
| `gender` | gender (0=F, 1=M) |
| `str2` | antiretroviral history (0=naive, 1=experienced). "Naive" indicates that the patient have had no prior experience with antiretroviral therapy (they are newly diagnosed or have not yet started treatment for HIV); while "experienced" indicates that the patient has had prior experience with antiretroviral drugs, meaning they have received antiretroviral treatments in the past (with continuous treatment over time or interrupted and restarted). |
| `strat` | antiretroviral history stratification (1 = 'Antiretroviral Naive', 2 = '> 1 but <= 52 weeks of prior antiretroviral therapy', 3 = '> 52 weeks') |
| `symptom` | symptomatic indicator (0=asymp, 1=symp) |
| `treat` | treatment indicator (0=ZDV only, 1=others) |
| `offtrt` | indicator of off-trt before 96+/-5 weeks (0=no,1=yes). Indicator related to treatment cessation (off-trt) within a specific period of time. |
| `cd40` | CD4 at baseline. CD4 is a surface protein found primarily on cells of the human immune system called helper T lymphocytes. HIV selectively attacks and destroys CD4+ cells, progressively weakening the immune system and making the body more vulnerable to opportunistic infections and other complications.Therefore, the count of CD4+ cells is used as an indicator to assess the severity of HIV infection and to monitor the progression of the disease over time. |
| `cd420` | CD4 at 20+/-5 weeks |
| `cd80` | CD8 at baseline. The CD8 is a surface protein found primarily on cells of the human immune system called cytotoxic T lymphocytes. These cells play a crucial role in defending the body against viral infections and tumor cells. |
| `cd820` | CD8 at 20+/-5 weeks |
| `infected` |  target variable. The patient is infected with AIDS (0=No, 1=Yes) |

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
