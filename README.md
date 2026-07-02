# nlp-logistics-classification-system
NLP-Based Customer Support Ticket Classification System 
## Overview

This project develops a Natural Language Processing (NLP) system to automatically classify customer support tickets for logistics and e-commerce companies. The system analyzes customer messages and predicts the appropriate support category, helping organizations improve response times, reduce manual workload, and streamline customer service operations.

The project follows a complete NLP workflow, including data preprocessing, feature engineering, model development, evaluation, and collaborative software development using GitHub.

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
- **Task:** Supervised text classification

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

- Clean and preprocess customer support text.
- Transform text into numerical feature vectors.
- Train and evaluate machine learning models.
- Compare feature extraction techniques.
- Maintain a well-documented GitHub repository.
- ---

## NLP Workflow

1. Data Collection
2. Data Cleaning
3. Text Preprocessing
4. Feature Engineering
5. Model Development
6. Model Evaluation
7. Prediction

---

## Data Preprocessing

The preprocessing pipeline prepares customer support messages for machine learning.

Typical preprocessing steps include:

- Lowercasing text
- Removing punctuation
- Tokenization
- Removing stop words (if applicable)
- Cleaning whitespace
- Preparing text for feature extraction

---
## Feature Engineering

Two feature extraction methods are currently available.

### Bag of Words (BoW)

Bag of Words converts text into numerical vectors based on word frequency.

### TF-IDF

TF-IDF (Term Frequency–Inverse Document Frequency) assigns greater importance to informative words while reducing the influence of common words.

Both feature extraction methods are available for experimentation and comparison during model development.

---
## Proposed Model Development

The current development plan includes:

- Train/test split
- Bag of Words vectorization
- TF-IDF vectorization
- Multinomial Naive Bayes model training
- Model evaluation
- Saving the trained model and vectorizer
- Prediction using new customer support tickets

The project will compare model performance using both Bag of Words and TF-IDF feature representations before selecting the final approach.

---

> **Work in Progress:** Model training and evaluation are still in progress. This section will be updated with final metrics and model comparisons before project completion.
## Planned Evaluation

Performance will be evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix


## Planned Model Comparison

| Model | Feature Representation | Accuracy | Precision | Recall | F1 Score |
|--------|------------------------|:--------:|:---------:|:------:|:--------:|
| Multinomial Naive Bayes | Bag of Words | TBD | TBD | TBD | TBD |
| Multinomial Naive Bayes | TF-IDF | TBD | TBD | TBD | TBD |
> **Work in Progress:**

## Repository Structure

```text
nlp-logistics-classification-system/
│
├── dashboards/
├── data/
├── docs/
├── notebooks/
├── src/
├── README.md
```

---
## GitHub Workflow

The project uses GitHub for collaboration through:

- Feature branches
- Pull requests
- Code reviews
- Version control

---
## Development Notes

The notebooks are numbered to reflect the workflow; however, Python cannot directly import functions from notebook filenames beginning with numbers.

### Vectorization Notes

Both **Bag of Words** and **TF-IDF** vectorizers are available.

During training:

```python
vectorizer.fit_transform(X_train)
```

During validation, testing, and prediction:

```python
vectorizer.transform(X_test)
```

Using `transform()` after training ensures the vocabulary remains consistent and prevents data leakage.

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

1. Load the dataset.
2. Run preprocessing.
3. Run feature engineering.
4. Train candidate models.
5. Evaluate model performance.
6. Compare feature extraction methods.
7. Predict new customer support tickets.

---
> **Work in Progress:** 
## Future Work
- Tune model hyperparameters.
- Evaluate additional classification models.
- Explore transformer-based NLP models.
- Deploy the model as a web application.
>
---

## Team

  
-  Alejandro Tovar Castillo
-  Galen Wu
-  Katie Price
-  Patricia Atkinson
  

---
## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Git & GitHub

## License

This project was developed for academic purposes as part of the IE7500 course.                
