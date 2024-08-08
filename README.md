
# Sentiment Analysis

A Kaggle notebook for the classification of Twitter messages into Positive, Negative, and Neutral using NLP and LSTM.

![Twitter Photo](https://paritkansal121.odoo.com/web/image/482-566b18cf/dataset-cover.webp)

## Kaggle Notebook
[Link to Notebook](https://www.kaggle.com/code/paritkansal/sentiment-analysis)

## Project Overview
This project focuses on entity-level sentiment analysis for Twitter messages. The objective is to determine the sentiment of each message concerning a specific entity. The dataset contains messages labeled with one of three sentiment classes: Positive, Negative, or Neutral. Messages that do not pertain to the entity are classified as Neutral. The project involves preprocessing the data, applying dimensionality reduction, and evaluating different machine learning models to effectively classify the sentiment of messages about the given entities.

## Project Description

### Data Loading and Exploration
- Loaded and inspected the dataset from `/kaggle/input/twitter-entity-sentiment-analysis/twitter_training.csv`.
- Cleaned the data by removing unnecessary columns and handling missing values.

### Dropping Extra Data
- Removed rows with missing values and unnecessary columns to prepare the dataset for further analysis.

### Pre-Processing
- Applied text preprocessing including:
  - Lowercasing
  - Emoji removal
  - HTML and URL stripping
  - Special character replacement
  - Contraction expansion
- Removed punctuation, stopwords, and performed lemmatization on the text data.

### PCA
- Used Principal Component Analysis (PCA) for dimensionality reduction on average word vectors derived from the comments.
- Visualized the reduced vectors in a 3D scatter plot.

### Model Development
- **Model 1: Embedding + Bidirectional LSTM**
  - Tokenized the text and padded sequences to prepare data for the model.
  - Built and trained a Bidirectional LSTM model with an embedding layer.

- **Model 2: Pre-trained Word2Vec + Bidirectional LSTM**
  - Loaded a pre-trained Word2Vec model to create an embedding matrix.
  - Built and trained a Bidirectional LSTM model using the pre-trained embeddings.

### Model Testing
- Evaluated the performance of both models on the test dataset:
  - **Model 1:**
    - Loss: 0.276157
    - Accuracy: 91.4%
  - **Model 2:**
    - Loss: 0.315279
    - Accuracy: 91.8%
