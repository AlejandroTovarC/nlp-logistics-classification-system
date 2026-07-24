# NLP-Based Customer Support Ticket Classification System

## Overview

This project develops a Natural Language Processing (NLP) system to automatically classify customer support tickets for logistics and e-commerce companies. The system analyzes customer messages and predicts the appropriate support category, helping organizations improve response times, reduce manual workload, and streamline customer service operations.

The project follows a complete NLP workflow, including data preprocessing, feature engineering, model training, evaluation, prediction, and collaborative software development using GitHub.

---

## Problem Statement

Logistics and e-commerce companies receive thousands of customer support requests related to delivery delays, damaged products, refund requests, billing inquiries, missing packages, technical issues, and other service-related concerns. Manually sorting these requests is time-consuming and inefficient.

The goal of this project is to develop a machine learning model capable of automatically classifying customer support tickets based on the customer's message.

---

## Dataset

The project uses the **Customer Support Tickets Dataset** available through Hugging Face.

### Dataset Summary

- **Source:** Hugging Face
- **Records:** 8,469
- **Task:** Supervised Text Classification

### Dataset Features

| Column |
|--------|
| Customer Email |
| Product Purchased |
| Ticket Type |
| Ticket Subject |
| Combined Text |
| Ticket Priority |

The **Combined Text** field is used as the primary input for model training.

---

## Project Objectives

- Clean and preprocess customer support ticket text.
- Transform text into numerical feature vectors using Bag-of-Words and TF-IDF.
- Train and evaluate Multinomial Naive Bayes classification models.
- Compare feature extraction techniques using multiple evaluation metrics.
- Save trained models and vectorizers for future predictions.
- Predict categories for new customer support tickets.
- Maintain a well-documented GitHub repository.

---

## NLP Workflow

1. Data Collection
2. Data Cleaning
3. Text Preprocessing
4. Feature Engineering
5. Model Development
6. Model Evaluation
7. Final Predictions

---

## Data Preprocessing

The preprocessing pipeline prepares customer support messages for machine learning.

The preprocessing steps include:

- Lowercasing text
- Removing punctuation
- Tokenization
- Removing stop words (if applicable)
- Cleaning whitespace
- Preparing text for feature extraction

---

## Feature Engineering

Two feature extraction techniques were implemented and compared.

### Bag-of-Words (BoW)

Bag-of-Words converts customer support messages into numerical vectors based on word frequency.

### TF-IDF

TF-IDF (Term Frequency–Inverse Document Frequency) assigns greater importance to informative words while reducing the influence of frequently occurring words.

Both techniques were evaluated using the same machine learning algorithm to determine the most effective representation for ticket classification.

---

## Model Development

The project includes:

- Train/test data split
- Bag-of-Words vectorization
- TF-IDF vectorization
- Multinomial Naive Bayes model training
- Model evaluation
- Saving trained models and vectorizers
- Predicting categories for new customer support tickets

---

## Model Evaluation

The trained models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Classification Report
- Confusion Matrix

The project compares the performance of the Bag-of-Words and TF-IDF feature representations using the same Multinomial Naive Bayes classifier.

---

## Model Comparison

The performance of the two feature extraction techniques was evaluated using a Multinomial Naive Bayes classifier.

| Model | Feature Representation | Accuracy | Precision | Recall | F1 Score |
|--------|------------------------|:--------:|:---------:|:------:|:--------:|
| Multinomial Naive Bayes | Bag-of-Words | **0.1882** | **0.1869** | **0.1882** | **0.1870** |
| Multinomial Naive Bayes | TF-IDF | 0.1742 | 0.1720 | 0.1742 | 0.1713 |

### Results Summary

The Bag-of-Words Multinomial Naive Bayes model outperformed the TF-IDF model across all evaluation metrics. Therefore, the Bag-of-Words model was selected as the final model for customer support ticket classification and prediction.
---

## Repository Structure

```text
nlp-logistics-classification-system/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── models/
│   ├── bow_naive_bayes_model.pkl
│   ├── tfidf_naive_bayes_model.pkl
│   ├── bow_vectorizer.pkl
│   └── tfidf_vectorizer.pkl
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_model_training.ipynb
│   ├── 05_model_evaluation.ipynb
│   └── 06_final_predictions.ipynb
│
├── dashboards/
├── docs/
├── src/
├── README.md
└── requirements.txt
```

---

## GitHub Workflow

The project uses GitHub for collaboration through:

- Feature branches
- Pull requests
- Code reviews
- Version control

---

## Installation

```bash
git clone https://github.com/AlejandroTovarC/nlp-logistics-classification-system
```

```bash
pip install -r requirements.txt
```

---

## Running the Project

Run the notebooks in the following order:

1. Data Exploration
2. Data Preprocessing
3. Feature Engineering
4. Model Training
5. Model Evaluation
6. Final Predictions

---

## Future Improvements

Potential enhancements include:

- Hyperparameter tuning
- Additional machine learning models
- Transformer-based NLP models (BERT)
- Web application deployment using Flask or Streamlit
- Real-time customer support ticket classification

---

## Team

- Alejandro Tovar Castillo
- Galen Wu
- Katie Price
- Patricia Atkinson

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Joblib
- Matplotlib
- Git
- GitHub

---

## License

This project was developed for academic purposes as part of the IE7500 Natural Language Processing course.