# Software Requirement Classification using Machine Learning

## Project Overview

This project aims to automatically classify software requirements into **Functional Requirements (FR)** and **Non-Functional Requirements (NFR)** using **Natural Language Processing (NLP)** and **Machine Learning** techniques.

Software requirements are typically written in natural language, making manual classification time-consuming and prone to errors. This project develops an end-to-end machine learning pipeline that preprocesses requirement text, extracts meaningful features, trains multiple classification models, and predicts the category of unseen software requirements.

---

# Problem Statement

Software Requirement Specifications (SRS) contain large numbers of textual requirements that must be categorized accurately. Manual classification is inefficient and may introduce inconsistencies.

The objective of this project is to automate this process by building a machine learning model capable of classifying software requirements as either:

* **Functional Requirement (FR)**
* **Non-Functional Requirement (NFR)**

---

# Project Objectives

* Collect and merge multiple software requirement datasets.
* Clean and preprocess textual requirement data.
* Perform Exploratory Data Analysis (EDA).
* Extract meaningful text features using TF-IDF.
* Select the most informative features using Chi-Square feature selection.
* Train and compare multiple machine learning models.
* Evaluate model performance using standard classification metrics.
* Develop a robust pipeline for automatic requirement classification.

---

# Dataset

The dataset was created by combining multiple publicly available software requirement datasets.

## Dataset Sources

* Functional and Non-Functional Requirement Dataset
* Extended Software Requirement Dataset
* Annotated Requirement Dataset

After merging and preprocessing:

* **Total Records:** 10,922
* **Features**

  * `sentence`
  * `label`
  * `length`
* **Target Variable**

  * `0` → Functional Requirement
  * `1` → Non-Functional Requirement

---

# Project Workflow

```text
Raw Datasets
      │
      ▼
Data Collection & Merging
      │
      ▼
Data Cleaning & Preprocessing
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
Text Vectorization (TF-IDF)
      │
      ▼
Feature Selection (Chi-Square)
      │
      ▼
Machine Learning Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Requirement Classification
```

---

# Data Preprocessing

The following preprocessing steps were performed:

* Dataset merging
* Duplicate removal
* Missing value handling
* Label standardization
* Lowercase conversion
* Punctuation removal
* Stopword removal
* Sentence length calculation
* Conflict detection and removal
* Outlier removal

---

# Exploratory Data Analysis

The dataset was analyzed to understand its characteristics through:

* Class distribution
* Requirement length distribution
* Word frequency analysis
* Label balance
* Statistical summaries
* Data visualization

---

# Feature Engineering

Textual requirements were converted into numerical features using:

* **TF-IDF Vectorization**

Feature dimensionality was reduced using:

* **Chi-Square Feature Selection**

---

# Machine Learning Models

Multiple classification algorithms were trained and compared, including:

* Logistic Regression
* Support Vector Machine (SVM)
* Naive Bayes
* Random Forest

The best-performing model was selected based on evaluation metrics.

---

# Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

These metrics were used to compare the performance of each classifier and identify the most effective model for software requirement classification.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* NLTK
* Matplotlib
* TF-IDF Vectorizer

---

# Project Structure

```text
Software-Requirement-Classification/
│
├── milestone-1/
│   ├── cleaned_dataset.csv
│   └── milestone1_data_collection_cleaning.ipynb
│
├── milestone-2/
│   ├── cleaned_dataset_v2.csv
│   └── milestone2_statistical_insights_feature_selection.ipynb
│
├── milestone-3/
│   ├── model_training_evaluation.ipynb
│   └── trained_model.pkl
│
├── README.md
└── requirements.txt
```

---

# Key Features

* Automated software requirement classification
* Natural Language Processing (NLP)
* Complete data preprocessing pipeline
* Exploratory Data Analysis (EDA)
* TF-IDF feature extraction
* Chi-Square feature selection
* Multiple machine learning models
* Performance comparison using evaluation metrics
* Predictive classification of new software requirements

---

# Future Improvements

* Deep Learning models (LSTM, Bi-LSTM, BERT)
* Multi-class requirement categorization
* Web-based prediction interface
* REST API deployment
* Real-time requirement classification
* Larger and more diverse datasets

---

# Conclusion

This project demonstrates how Natural Language Processing and Machine Learning can automate software requirement classification. By integrating data preprocessing, feature engineering, model training, and evaluation into a single pipeline, the system reduces manual effort and provides a scalable approach for analyzing Software Requirement Specifications (SRS). The project showcases practical applications of NLP in software engineering and highlights the effectiveness of machine learning for improving requirement analysis.
