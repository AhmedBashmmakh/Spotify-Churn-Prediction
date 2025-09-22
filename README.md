# Spotify Churn Analysis Project

## Project Overview

This project analyzes a Spotify user dataset to explore factors that influence churn and builds predictive models to classify whether a user is likely to churn.

## Dataset

* **Source:** `spotify_churn_dataset.csv`
  You can download the dataset from Kaggle: [Spotify Churn Dataset](https://www.kaggle.com/datasets/nabihazahid/spotify-dataset-for-churn-analysis)
* **Features:**

  * `user_id`: Unique identifier for each user
  * `gender`: Gender of the user
  * `age`: Age of the user
  * `country`: Country of the user
  * `subscription_type`: Type of subscription (Free, Premium, etc.)
  * `listening_time`: Total listening time (hours)
  * `songs_played_per_day`: Average songs played per day
  * `skip_rate`: Fraction of songs skipped
  * `device_type`: Device used for listening
  * `ads_listened_per_week`: Number of ads listened to per week
  * `offline_listening`: Whether user listens offline (Yes/No)
  * `is_churned`: Target variable (1 = churned, 0 = retained)

## Project Steps

### 1. Exploratory Data Analysis (EDA)

* Check missing values and duplicates
* Summary statistics and dataset shape
* Visualizations:

  * Subscription type distribution
  * Age distribution by churn status
  * Device type usage vs churn
  * Top 10 countries by churn
  * Correlation heatmap of numeric features

### 2. Data Preprocessing

* Identify numeric and categorical columns
* Standardize numeric features using `StandardScaler`
* One-hot encode categorical features using `OneHotEncoder`
* Use `ColumnTransformer` to combine preprocessing steps

### 3. Machine Learning Models

* Models used:

  * K-Nearest Neighbors (KNN)
  * Decision Tree Classifier
  * Random Forest Classifier
  * Logistic Regression
* Hyperparameter tuning with `GridSearchCV`
* Train/test split (80% train, 20% test)
* Handle class imbalance with `class_weight='balanced'` for relevant models

### 4. Model Evaluation

* Metrics:

  * Accuracy
  * Classification report (precision, recall, F1-score)
* Summary table comparing model performance
* Optionally visualize confusion matrices and feature importance



## Notes

* The dataset may be imbalanced; using class weighting helps mitigate bias toward majority class.
* EDA visualizations help identify patterns related to churn.
* Hyperparameter tuning improves model performance.
