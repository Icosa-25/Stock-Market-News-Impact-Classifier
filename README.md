# Stock Market News Impact Classifier

An NLP and machine learning-based project that classifies financial news headlines into **LOW, MEDIUM, and HIGH impact categories** based on their potential market relevance.

## Project Overview

Financial markets react continuously to news related to companies, monetary policy, economic events, and market developments. However, not every news headline has the same level of potential market impact.

This project builds a machine learning pipeline to classify financial news into three impact categories:

- **LOW** – News expected to have relatively low market impact
- **MEDIUM** – News with moderate potential market relevance
- **HIGH** – News associated with potentially significant market impact

The project combines **Natural Language Processing (NLP)** with engineered numerical features extracted from financial news headlines.

## Project Notebook

The complete implementation, including data analysis, feature engineering, model training, evaluation, class-imbalance handling, and fresh-news inference, is available in:

**[Stock_Market_News_Impact_Classifier.ipynb](Stock_Market_News_Impact_Classifier.ipynb)**

## Machine Learning Pipeline

The project follows the following workflow:

`Financial News → Text Cleaning → Feature Engineering → TF-IDF → Model Training → Impact Classification`

The models explored include:

- Multinomial Naive Bayes
- Logistic Regression
- Random Forest

The dataset contains a significant class imbalance, particularly for the HIGH-impact category. Techniques such as class weighting and SMOTE were explored to improve minority-class detection.

## Features

The model uses TF-IDF representations of cleaned financial headlines along with engineered features such as:

- Percentage values mentioned in headlines
- Monetary values
- Headline length
- Word count
- Negation indicators

The `relevance_score` feature was excluded from model inputs after analysis showed a deterministic relationship with the target `impact_tier`, which could introduce target leakage.

## Fresh News Inference

The project also includes integration with NewsAPI to fetch recent financial news headlines and pass them through the trained classification pipeline.

The API key is intentionally not included in this repository for security reasons.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- TF-IDF
- Imbalanced-learn / SMOTE
- Matplotlib
- Seaborn
- NewsAPI

## Disclaimer

This project predicts **news impact categories (LOW, MEDIUM, HIGH)** and does not directly predict stock price direction or provide financial or investment advice.

## How to Run

1. Clone this repository.
2. Install the required dependencies:

   pip install -r requirements.txt

3. Place the required dataset (`stk.csv`) in the appropriate project directory.
4. Open `Stock_Market_News_Impact_Classifier.ipynb` in Jupyter Notebook.
5. Run the notebook cells sequentially.

For fresh-news inference using NewsAPI, configure your own API key securely as an environment variable. API credentials are not included in this repository.
