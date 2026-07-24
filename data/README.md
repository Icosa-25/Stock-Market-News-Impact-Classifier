# Dataset

This project uses a financial news dataset containing 139,919 records for training and evaluating the news impact classification model.

## Dataset Features

The dataset contains information such as:

- Date
- News title
- News description
- Source information
- News categories
- Matched financial keywords
- Relevance score
- Negation indicator
- Impact tier

The target variable is:

`impact_tier`

with three classes:

- LOW
- MEDIUM
- HIGH

## Important Note

The `relevance_score` feature was excluded from the model input after exploratory analysis showed a deterministic relationship between `relevance_score` and `impact_tier`, which could introduce target leakage.

The dataset file is not included directly in this repository due to dataset size and data-distribution considerations.

To reproduce the project, place the dataset in the project directory and update the dataset path in the notebook if required.
