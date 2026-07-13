# Software Requirement Classification using Machine Learning

## Project Overview

This project presents an end-to-end **Natural Language Processing (NLP)** and **Machine Learning** pipeline for automatically classifying software requirements into **Functional Requirements (FR)** and **Non-Functional Requirements (NFR)**.

Software Requirement Specifications (SRS) are typically written in natural language, making manual classification time-consuming, inconsistent, and prone to human error. This project automates the classification process using text preprocessing, feature engineering, and multiple supervised machine learning algorithms.

---

# Problem Statement

Software Requirement Specifications contain hundreds or even thousands of textual requirements that must be categorized accurately during software development.

Manual classification of software requirements is:

- Time-consuming
- Error-prone
- Difficult to maintain for large-scale software projects

The objective of this project is to automatically classify software requirements into:

- Functional Requirements (FR)
- Non-Functional Requirements (NFR)

using Natural Language Processing and Machine Learning techniques.

---

# Project Objectives

- Collect and merge multiple software requirement datasets.
- Perform data cleaning and preprocessing.
- Conduct Exploratory Data Analysis (EDA).
- Convert textual requirements into numerical features using TF-IDF.
- Perform feature selection using Chi-Square statistics.
- Train and compare multiple machine learning models.
- Evaluate model performance using weighted evaluation metrics.
- Develop an automated software requirement classification pipeline.

---

# Dataset

The dataset was created by combining three publicly available software requirement datasets.

## Dataset Sources

- PURE Requirements Dataset
- Software Requirements Dataset
- Extended Software Requirements Dataset

After merging:

- **Original Dataset:** 12,973 software requirements

After preprocessing and cleaning:

- **Final Dataset:** 10,618 software requirements

---

## Features

| Feature | Description |
|----------|-------------|
| sentence | Software requirement statement |
| label | Target class (0 = FR, 1 = NFR) |

### Target Variable

| Label | Requirement Type |
|--------|------------------|
| 0 | Functional Requirement |
| 1 | Non-Functional Requirement |

---

# Project Workflow

```text
Raw Datasets
      │
      ▼
Dataset Collection & Merging
      │
      ▼
Data Cleaning & Preprocessing
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
TF-IDF Feature Engineering
      │
      ▼
Chi-Square Feature Selection
      │
      ▼
Train-Test Split
      │
      ▼
Machine Learning Model Training
      │
      ▼
Performance Evaluation
      │
      ▼
Requirement Classification
```

---

# Data Preprocessing

The following preprocessing steps were performed:

- Dataset merging
- Duplicate removal
- Missing value handling
- Label standardization
- Lowercase conversion
- Special character removal
- Punctuation removal
- Tokenization
- Stopword removal
- Sentence cleaning

These preprocessing steps reduced dataset noise and improved textual consistency before feature extraction.

---

# Exploratory Data Analysis (EDA)

The dataset was analyzed using:

- Class distribution analysis
- Requirement length analysis
- Word frequency analysis
- Statistical summaries
- Dataset visualization
- Label distribution analysis

---

# Feature Engineering

Textual software requirements were converted into numerical feature vectors using **TF-IDF (Term Frequency–Inverse Document Frequency)**.

Initially, TF-IDF generated **1000 textual features**.

To reduce dimensionality and retain only the most informative features, **Chi-Square Feature Selection** was applied.

- Original Features: **1000**
- Selected Features: **500**

These selected features were then used to train the machine learning models.

---

# Experimental Setup

Three different experimental configurations were conducted.

## Experiment 1 – Baseline Dataset

- Original dataset
- No preprocessing
- No feature selection

---

## Experiment 2 – Cleaned Dataset

- Data preprocessing applied
- TF-IDF feature extraction
- No feature selection

---

## Experiment 3 – Cleaned Dataset + Feature Selection

- Data preprocessing
- TF-IDF vectorization
- Chi-Square feature selection

This configuration was used for the complete comparison of machine learning classifiers.

---

# Machine Learning Models

The following supervised learning algorithms were implemented and compared:

- Logistic Regression
- Naive Bayes
- Random Forest
- K-Nearest Neighbors (KNN)
- Linear Support Vector Classifier (Linear SVC)
- XGBoost

---

# Model Evaluation

The models were evaluated using:

- Accuracy
- Weighted Precision
- Weighted Recall
- Weighted F1-Score
- Classification Report
- Normalized Confusion Matrix

Weighted evaluation metrics were used because the dataset contains an imbalanced distribution of Functional and Non-Functional Requirements.

---

# Results

| Model | Accuracy |
|--------|----------|
| Logistic Regression | 84.09% |
| Naive Bayes | 84.89% |
| Random Forest | **86.96%** |
| K-Nearest Neighbors | 84.13% |
| Linear SVC | 83.62% |
| XGBoost | 85.88% |

### Key Findings

- Random Forest achieved the highest overall Accuracy and Weighted F1-Score.
- Linear SVC achieved the highest recall for Non-Functional Requirements.
- Data preprocessing significantly improved classification performance.
- Chi-Square feature selection reduced dimensionality while maintaining competitive performance.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Matplotlib
- XGBoost
- TF-IDF Vectorizer

---

# Project Structure

```text
Software-Requirement-Classification/
│
├── milestone-1/
│   ├── cleaned_dataset.csv
│   └── Data_Merging_and_Cleaning.ipynb
│
├── milestone-2/
│   ├── cleaned_dataset_v2.csv
│   └── Statistical_Insights_and_Feature_Selection.ipynb
│
├── milestone-3/
│   ├── final_experiment_ibcast.ipynb
│   ├── DSE_Term_Paper.pdf
│   └── README.md
│
├── requirements.txt
└── LICENSE
```

---

# Key Features

- Automated Software Requirement Classification
- Natural Language Processing (NLP)
- End-to-End Machine Learning Pipeline
- Exploratory Data Analysis (EDA)
- TF-IDF Feature Engineering
- Chi-Square Feature Selection
- Comparative Machine Learning Analysis
- Weighted Performance Evaluation
- Normalized Confusion Matrix
- Research-Oriented Experimental Framework

---

# Future Improvements

Possible extensions of this work include:

- Deep Learning models (LSTM, Bi-LSTM)
- Transformer-based models (BERT, RoBERTa)
- Multi-class requirement classification
- REST API deployment
- Web-based prediction interface
- Real-time requirement classification
- Larger and more diverse software requirement datasets

---

# Conclusion

This project demonstrates the effectiveness of combining **Natural Language Processing (NLP)** and **Machine Learning** for automatic software requirement classification. By integrating data preprocessing, TF-IDF feature engineering, Chi-Square feature selection, and comparative evaluation of multiple machine learning models, the proposed pipeline provides a scalable and effective solution for analyzing Software Requirement Specifications (SRS). The project highlights the practical application of AI in Software Engineering and contributes toward improving automated requirement analysis.
