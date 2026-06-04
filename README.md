# Fake News Predictor 📰🚨

## Overview
This repository contains a Machine Learning and Natural Language Processing (NLP) project designed to classify news articles as either **Real** or **Fake**. The model processes textual data from news articles and uses a Logistic Regression algorithm to make predictions.

## Dataset
* **Data Source:** The project expects a dataset named `train.csv`.
* **Key Features:** The model merges the `author` and `title` columns into a single `content` feature for training.
* **Target Labels:** * `0`: Real News
  * `1`: Fake News

## Tech Stack
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:** * `NumPy` & `Pandas` for data handling.
  * `NLTK` (Natural Language Toolkit) for text preprocessing (Stopwords, PorterStemmer).
  * `Scikit-Learn` for feature extraction (`TfidfVectorizer`), model training, and evaluation.

## Data Preprocessing Workflow
To ensure the text data is ready for the machine learning model, the following NLP techniques are applied:
1. **Handling Missing Values:** Null values are replaced with empty strings.
2. **Feature Engineering:** Merging the author's name and article title.
3. **Text Cleaning:** Removing numbers, punctuation, and special characters using Regular Expressions (`re`).
4. **Lowercasing:** Converting all text to lowercase for consistency.
5. **Stopword Removal:** Filtering out common English words (like "the", "a", "is") that do not add predictive value.
6. **Stemming:** Reducing words to their root/base form using `PorterStemmer` (e.g., "running" becomes "run").
7. **Vectorization:** Converting the cleaned text into numerical data using Term Frequency-Inverse Document Frequency (`TF-IDF`).

## Model Performance
The dataset is split into 80% training data and 20% testing data, stratified to maintain class balance.
* **Algorithm:** Logistic Regression
* **Training Data Accuracy:** ~98.6%
*
