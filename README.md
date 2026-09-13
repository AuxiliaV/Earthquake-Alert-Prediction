# Earthquake Alert Prediction System

Machine learning classification project for predicting earthquake alert categories using historical earthquake data.

## Project Overview

This capstone project follows an end-to-end machine learning workflow: data preprocessing and exploratory analysis, feature selection, model comparison, hyperparameter tuning, evaluation, model serialization, and prediction.

The final model is a Decision Tree Classifier using **magnitude**, **significance (`sig`)**, and **depth** to predict four alert categories: Green, Yellow, Orange, and Red.

> This is a personal/capstone project demonstrating machine-learning skills. It is not presented as a real-time earthquake early-warning or emergency-response system.

## Dataset

Source: [Kaggle Earthquake Dataset](https://www.kaggle.com/datasets/warcoder/earthquake-dataset)

The project report describes the dataset as covering 1 January 2001 to 1 January 2023, with 782 records and 19 columns.

The dataset files are not included in this repository. See [`data/README.md`](data/README.md) for setup instructions.

## Workflow

```text
Raw Earthquake Data
        ↓
Preprocessing & EDA
        ↓
Feature Selection
        ↓
Model Comparison & Hyperparameter Tuning
        ↓
Decision Tree Classifier
        ↓
Model Evaluation
        ↓
Saved .sav Model
        ↓
Prediction Workflow
```

## Feature Selection

Candidate features included magnitude, sig, dmin, gap, and depth. The project used multiple feature-selection approaches. The preferred three-feature combination was **magnitude + sig + depth**.

## Models Compared

- Logistic Regression
- Support Vector Machine
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors
- Gaussian Naive Bayes

`GridSearchCV` was used for hyperparameter tuning.

## Final Model

**Algorithm:** Decision Tree Classifier  
**Features:** magnitude, sig, depth  
**Reported accuracy:** approximately 84%  
**Weighted F1-score:** approximately 0.835 on the reported test evaluation  

## Repository Structure

```text
├── README.md
├── notebooks/
│   ├── 01_Data_Preprocessing_and_EDA.ipynb
│   ├── 02_Feature_Selection.ipynb
│   ├── 03_Model_Identification.ipynb
│   ├── 04_Model_Creation.ipynb
│   └── 05_Model_Deployment.ipynb
├── model/
│   └── earthquake_alert_prediction.sav
├── data/
│   └── README.md
├── screenshots/
├── requirements.txt
└── .gitignore
```

## Technologies

Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Scikit-learn, mlxtend, Jupyter Notebook, Pickle.

## Author

**Auxilia V**  
GitHub: [AuxiliaV](https://github.com/AuxiliaV)
