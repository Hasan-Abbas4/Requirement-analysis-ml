# Software Requirement Analysis using Machine Learning

## Project Overview
This project focuses on analyzing software requirements and classifying them into **Functional Requirements (FR)** and **Non-Functional Requirements (NFR)** using data science and machine learning techniques. The goal is to build a structured pipeline for requirement preprocessing, analysis, feature engineering, and predictive modeling.

Software requirements are critical in software engineering because they define the expected behavior, features, and quality attributes of a software system. Correctly identifying and analyzing these requirements helps improve software planning, quality assurance, and development efficiency.

---

## Problem Statement
Software requirements are often written in natural language, making them difficult to analyze automatically. Misclassification of requirements can cause misunderstandings, poor system design, and project failures. This project aims to automate the classification and analysis of software requirements to improve software engineering processes.

---

## Project Objectives
- Build a classification-ready dataset of software requirements.
- Analyze requirement patterns using statistical insights.
- Apply feature extraction and feature selection techniques.
- Perform clustering to identify similar requirement groups.
- Prepare the dataset for machine learning modeling and evaluation.

---

## Dataset Sources
The project uses multiple public datasets collected from Kaggle and merged into one unified dataset.

### Dataset 1
Requirement dataset containing Functional and Non-Functional Requirements.

### Dataset 2
Extended software requirement dataset with labeled requirement categories.

### Dataset 3
Annotated requirement dataset for functional and non-functional classification.

---

## Final Dataset Statistics
After preprocessing and cleaning:

- Total records: **10,922**
- Features:
  - `sentence`
  - `label`
  - `length`
- Target Variable:
  - `0` → Functional Requirement
  - `1` → Non-Functional Requirement

---

## Project Milestones

## Milestone 1 — Data Collection and Cleaning
Tasks completed:
- Collected datasets from multiple sources
- Merged datasets into a single dataset
- Standardized labels into binary format
- Removed null values
- Removed punctuation
- Converted text to lowercase
- Initial duplicate removal

Files:
- `cleaned_dataset.csv`
- `milestone1_data_collection_cleaning.ipynb`

---

## Milestone 2 — Statistical Insights and Feature Selection
Tasks completed:
- Exploratory Data Analysis (EDA)
- Class distribution analysis
- Requirement sentence length analysis
- Word frequency analysis
- Stopword removal
- Outlier removal
- Duplicate validation and removal
- Conflict detection and removal
- TF-IDF feature extraction
- Chi-Square feature selection
- K-Means clustering

Files:
- `cleaned_dataset_v2.csv`
- `milestone2_statistical_insights_feature_selection.ipynb`

---

## Data Science Techniques Used
- Data Cleaning
- Data Preprocessing
- Exploratory Data Analysis (EDA)
- Natural Language Processing (NLP)
- TF-IDF Feature Extraction
- Chi-Square Feature Selection
- Clustering (K-Means)

---

## Machine Learning Pipeline
```text
Raw Data
↓
Data Cleaning
↓
Statistical Analysis
↓
Feature Extraction (TF-IDF)
↓
Feature Selection (Chi-Square)
↓
Clustering
↓
Model Training (Upcoming)
↓
Evaluation (Upcoming)
