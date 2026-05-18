# HIV/AIDS Patient Machine Learning Analysis

This repository contains an exploratory data analysis and machine learning project based on a healthcare dataset related to HIV/AIDS patient records.

The analysis investigates clinical and categorical patient information, performs preprocessing and feature analysis, addresses class imbalance, and compares different machine learning models for binary classification.

> This project is intended for educational and portfolio purposes only. It is not intended to provide medical advice, diagnosis, or clinical decision support.

## Context

In 1996, an important medical study involved patients with HIV/AIDS in order to evaluate the effectiveness of different antiretroviral treatments. Patients were divided into four treatment groups, each receiving a different experimental therapeutic regimen. The objective was to analyze patient information and treatment outcomes, with particular attention to whether patients were classified as infected after treatment.

This clinical context provides the basis for a machine learning evaluation of the data.

---

## Dataset Overview

The dataset contains healthcare statistics and categorical information about patients involved in an AIDS-related study.
It includes clinical measurements, demographic information, treatment-related variables, and binary/categorical indicators describing patient conditions and treatment history. In this project, the version with 5,000 instances and 23 features was used. 

The target variable is:

- `infected`: binary classification target. 

The dataset was obtained from Kaggle and is related to the following clinical article:

- Dataset source: [Kaggle - AIDS Virus Infection Prediction](https://www.kaggle.com/datasets/aadarshvelu/aids-virus-infection-prediction/data)
- Related article/reference: [A trial comparing nucleoside monotherapy with combination therapy in HIV-infected adults with CD4 cell counts from 200 to 500 per cubic millimeter.](10.1056/NEJM199610103351501)

For licensing and privacy reasons, the dataset is not included in this repository.  
Please download it directly from Kaggle before running the notebook.

---

## Attribute Information

 The dataset contains the following attributes:

| Attribute | Description |
|---|---|
| `time` | time to failure or censoring. It indicates the time elapsed until the event of interest occurs, or the censoring time if the event has not been observed. |
| `trt` | treatment group indicator: 0 = ZDV, 1 = ZDV + ddI, 2 = ZDV + Zal, 3 = ddI. Where ZDV = zidovudine, ddI = didanosine, Zal = zalcitabine. |
| `age` | age (yrs) at baseline. |
| `wtkg` | weight (kg) at baseline. |
| `hemo` | hemophilia indicator: 0=no, 1=yes. |
| `homo` | homosexual activity indicator: 0=no, 1=yes. |
| `drugs` | history of IV drug use: 0=no, 1=yes. |
| `karnof` | Karnofsky score (on a scale of 0-100). It is a system used to evaluate the functional status and autonomy of a patient with a disease. |
| `oprior` | Non-ZDV antiretroviral therapy pre-175: 0=no, 1=yes. So, it evaluates whether the patient has undergone non-zidovudine-based antiretroviral therapy prior to initiating treatment (175 weeks earlier). |
| `z30` | indicator of whether ZDV was administered in the 30 days before the 175-week observation mark: 0=no, 1=yes. |
| `preanti` | days pre-175 antiretroviral therapy. Number of days or the duration that a patient has been on anti-retroviral therapy before reaching the 175-week mark since the start of observation or treatment. |
| `race` | race indicator: 0=white, 1=non-white. |
| `gender` | gender indicator: 0=F, 1=M. |
| `str2` | antiretroviral history: 0=naive, 1=experienced. |
| `strat` | antiretroviral history stratification: 1 = 'Antiretroviral Naive', 2 = '> 1 but <= 52 weeks of prior antiretroviral therapy', 3 = '> 52 weeks'.|
| `symptom` | symptomatic indicator: 0=asymp, 1=symp. |
| `treat` | treatment indicator: 0=ZDV only, 1=others. |
| `offtrt` | indicator of off-trt before 96+/-5 weeks: 0=no,1=yes. |
| `cd40` | CD4 cell count at baseline. CD4 is a surface protein found primarily on cells of the human immune system called helper T lymphocytes. HIV selectively attacks and destroys CD4+ cells, progressively weakening the immune system and making the body more vulnerable to opportunistic infections and other complications. Therefore, the count of CD4+ cells is used as an indicator to assess the severity of HIV infection and to monitor the progression of the disease over time. |
| `cd420` | CD4 cell count at 20+/-5 weeks. |
| `cd80` | CD8 cell count at baseline. The CD8 is a surface protein found primarily on cells of the human immune system called cytotoxic T lymphocytes. These cells play a crucial role in defending the body against viral infections and tumor cells. |
| `cd820` | CD8 cell count at 20+/-5 weeks. |
| `infected` |  target variable. The patient is infected with AIDS: 0=No, 1=Yes. |

---

## Project Goals

- Explore and understand the HIV/AIDS healthcare dataset
- Preprocess the data for machine learning analysis
- Handle class imbalance using oversampling techniques
- Train and compare different classification models
- Evaluate model performance using appropriate classification metrics
- Identify the best-performing model for infection outcome prediction

---

## Methodology

The project follows these main steps:

1. Dataset loading and initial inspection
2. Exploratory Data Analysis
3. Feature analysis and visualization
4. Missing value and outlier analysis
5. Categorical feature encoding
6. Correlation and feature importance analysis
7. Dataset preprocessing for machine learning
8. Class imbalance handling using oversampling
9. Model training and comparison
10. Hyperparameter tuning
11. Model evaluation using classification metrics, confusion matrices, and learning curves

---

## Class Imbalance Handling

The target classes were imbalanced in the original dataset. To address this issue, Random Oversampling was applied to the minority class.

| Dataset version | Class 0 | Class 1 |
|---|---:|---:|
| Original dataset | 3421 | 1579 |
| After oversampling | 3421 | 3421 |

---

## Machine Learning Models

The following classification models were tested:

- Random Forest
- Decision Tree
- Support Vector Classifier
- Logistic Regression
- K-Nearest Neighbors
- Multi-Layer Perceptron

They were evaluated using repeated stratified cross-validation on the training set and a final evaluation on the test set.

---

## Results

The models were compared using accuracy, classification reports, confusion matrices, and learning curves.

| Model | Mean CV Accuracy ± Std | Test Accuracy |
|---|---:|---:|
| Random Forest | 0.7894 ± 0.0135 | 0.81 |
| Decision Tree | 0.7338 ± 0.0154 | 0.76 |
| SVC | 0.6471 ± 0.0088 | 0.71 |
| Logistic Regression | 0.6221 ± 0.0130 | 0.63 |
| K-Nearest Neighbors | 0.6464 ± 0.0109 | 0.74 |
| MLP Classifier | 0.6617 ± 0.0095 | 0.77 |
| TensorFlow MLP | 0.6572 ± 0.0137 | 0.65 |

Random Forest showed the most reliable performance in the main comparison, achieving the highest mean cross-validation accuracy and the best test-set accuracy. However, the hyperparameter search was performed on a limited search space. Therefore, the selected configuration should not be considered globally optimal, and further tuning could potentially improve the results.
In some experiments, models trained with default parameters, especially Random Forest and Logistic Regression, also showed competitive performance. This suggests that model behavior may depend on the selected hyperparameter search space and evaluation setting.

Detailed outputs are available in the notebook.

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- TensorFlow / Keras

---

## How to Run

1. Clone the repository.
2. Install the main Python dependencies:
   pip install -r requirements.txt
3. Download the dataset from Kaggle:
   Kaggle - AIDS Virus Infection Prediction
5. Open and run the Jupyter notebook.

---

## Future Developments

- Integrate the full preprocessing workflow into a machine learning pipeline
- Apply resampling techniques only within the training process to avoid data leakage
- Expand the hyperparameter search space
- Test additional models and evaluation strategies
- Compare performance on larger versions of the dataset
