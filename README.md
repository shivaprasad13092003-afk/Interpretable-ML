I can help you create a README file for your GitHub upload based on the provided document. Here's a draft:

``` markdown
# Interpretable ML for Customer Segmentation

This repository contains the code and resources for a summer project focused on developing an interpretable machine learning (IML)-based approach for customer segmentation using online product reviews.

## Project Overview

This study proposes an interpretable machine learning approach for customer segmentation, utilizing the importance of product features extracted from online reviews. Unlike previous methods that relied on demographic, psychographic, or general sentiment data, this project aims to identify nonlinear relationships and common unsatisfied needs for new product development.

## Content

The project workflow includes:
1.  **Overview**: Introduction to the project's goals and motivation.
2.  **Data Collection & Preprocessing**: Details on scraping hotel reviews from Booking.com and text preprocessing steps (tokenization, cleaning, lemmatization, emoji conversion).
3.  **Exploratory Data Analysis (EDA)**: Analysis of the collected dataset, including its shape, data types, and distribution of key features like "Nights Stayed," "Stayed Month," "Review Score," and "Hotel Name."
4.  **Feature Identification**: Method for identifying key product features from review text using Chunking, Affinity Propagation (AP) Clustering, and Hierarchical Clustering.
5.  **Sentiment Estimation**: Analysis of sentiment (positive, negative, neutral) for identified features using VADER, and visualization of positive/negative review counts per feature.
6.  **ML Classifiers and Cross Validation**: Implementation and evaluation of various machine learning classifiers (Decision Trees, Random Forest, LGBM, XGBoost, CatBoost) to predict star ratings, with a focus on nested cross-validation for hyperparameter optimization.
7.  **Feature Importance**: Explanation and application of SHAP (SHapley Additive exPlanations) to understand how each feature contributes to the model's predictions, particularly with the best-performing Random Forest model.
8.  **Customer Segmentation**: Grouping of hotel reviews using K-Means clustering based on feature importance, satisfaction, and opportunity scores to identify areas for improvement.

## Data

*   **Source**: 11,576 hotel reviews collected from four luxury hotels in London via Booking.com.
*   **Features**: The dataset includes 12 features such as Hotel Name, Reviewer Name, Home Town, Traveler Type, Room Type, Nights Stayed, Stayed Month, Reviewed Date, Review Title, Positive Feedback, Negative Feedback, and Review Score.

## Methodology

### Data Preprocessing
*   Text converted to lowercase and tokenized.
*   Punctuation and stop words removed.
*   Lemmatization applied; emojis converted to text.

### Feature Identification
*   **Chunking & AP Clustering**: Breaks down review word vectors, clusters similar words, and identifies exemplars.
*   **Hierarchical Clustering**: Refines clusters of exemplars.
*   **Feature Identification**: Determines key features by finding words closest to cluster centroids.

### Sentiment Estimation
*   VADER used to analyze sentiment of sentences mentioning identified features.
*   Sentiment scores (ranging from -1 to +1) combined to determine overall feedback.

### Machine Learning
*   **Classifiers**: Decision Trees, Random Forest, LGBM, XGBoost, and CatBoost were trained to predict star ratings.
*   **Nested Cross-Validation**: Employed to optimize hyperparameters and ensure robust performance evaluation.
*   **Evaluation Metric**: F1-score was used to assess prediction performance. Random Forest was selected as the top-performing model (F1 Score: 0.9298).

### Interpretable ML
*   **SHAP (SHapley Additive exPlanations)**: Used to explain the predictions of the Random Forest model by quantifying the contribution of each product feature to the predicted star rating.

### Customer Segmentation
*   **K-Means Clustering**: Applied to group reviews based on the importance of features.
*   **Opportunity Score**: Calculated using the formula `Opportunity = Importance + max(Importance - Satisfaction, 0)` to highlight features important to customers but not meeting their expectations.

## Results

*   Random Forest achieved the highest F1-score (0.9298) among the tested classifiers.
*   SHAP analysis provided insights into the influence of individual features on customer satisfaction.
*   Customer segmentation revealed distinct customer groups with varying levels of importance and satisfaction across different hotel features, identifying key areas for potential improvement (e.g., "manager," "bathroom," "service," "price" showing high opportunity scores in some clusters).

## Group Members

*   Vishnu Vardhan (21CE3AI13)
*   Gowtham Chowdary (21CE10084)
*   Harvin Raj (21ME10090)
*   Shiva Prasad (21ME31072)

```
