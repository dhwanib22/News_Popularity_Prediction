# News Popularity Prediction

## Problem Description

This repository contains a large dataset of news items and their respective social feedback on multiple platforms, including Facebook, Google+, and LinkedIn. The dataset spans a period of 8 months, from November 2015 to July 2016, encompassing around 100,000 news items across four different topics: Economy, Microsoft, Obama, and Palestine.

### Approaches Used

- **Popularity Prediction**
- **Sentiment Analysis**

## Preprocessing

- Outlier Treatment and Standardization- Quantile Method for outlier treatment
- Cleaning the text column ('reviewText') by:
  - Removing stop words
  - Converting text to lowercase
  - Removing punctuation and numbers
  - Tokenizing
  - Stemming
  - Lemmatization

Utilizing TF-IDF vectorization.

## Model Performance

### Popularity Prediction

The linear regression model outperformed others with the following metrics:

- **Mean Squared Error (MSE):**
  - Facebook: 0.7063
  - LinkedIn: 0.8590
  - GooglePlus: 0.8978

- **R-squared (R2):**
  - Facebook: 0.1831
  - LinkedIn: 0.1013
  - GooglePlus: 0.0847

### Sentiment Analysis

Random Forest model achieved the best results:

- **Accuracy Score:**
  - Title: 70%
  - Headline: 72%

Poor performance was observed in RNN and LSTM models, but BiLSTM showed improvement:

- **Accuracy Score:**
  - Title: 68%
  - Headline: 71%

## Conclusions

### Business Problem Solutions

Based on exploratory data analysis (EDA) inferences:

- Recommend posting news on Facebook regarding Obama between 14:00 till midnight on Saturdays for increased popularity.
- Suggest posting news on LinkedIn about Microsoft on Mondays for improved popularity.

Based on model inferences:

- Before publishing any news, users can check its predicted popularity on a specific platform.
- Higher popularity scores are desirable, and while negative sentiment news tends to be more popular, positive sentiment news can have a greater impact.
