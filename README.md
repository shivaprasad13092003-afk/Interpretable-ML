# Interpretable ML for Customer Segmentation

This repository contains the code and resources for a summer project focused on developing an interpretable machine learning based approach for customer segmentation using online product reviews.

## Project Overview

This study proposes an interpretable machine learning approach for customer segmentation, utilizing the importance of product features extracted from online reviews. Unlike previous methods that relied on demographic, psychographic, or general sentiment data, this project aims to identify nonlinear relationships and common unsatisfied needs for new product development.

## Contents

1. Overview – Introduction to the project goals and motivation  
2. Data Collection and Preprocessing – Scraping hotel reviews from Booking.com and text preprocessing including tokenization, cleaning, lemmatization, and emoji conversion  
3. Exploratory Data Analysis – Dataset analysis including its shape, data types, and distribution of features such as Nights Stayed, Stayed Month, Review Score, and Hotel Name  
4. Feature Identification – Identifying key product features using Chunking, Affinity Propagation Clustering, and Hierarchical Clustering  
5. Sentiment Estimation – Sentiment analysis using VADER and visualization of review counts per feature  
6. Machine Learning Classifiers and Cross Validation – Training and evaluation of Decision Trees, Random Forest, LGBM, XGBoost, and CatBoost using nested cross validation  
7. Feature Importance – Application of SHAP to interpret Random Forest predictions  
8. Customer Segmentation – K Means clustering of reviews based on feature importance, satisfaction, and opportunity scores  

## Data

Source: 11,576 hotel reviews collected from four luxury hotels in London via Booking.com  
Features: 12 attributes including Hotel Name, Reviewer Name, Home Town, Traveler Type, Room Type, Nights Stayed, Stayed Month, Reviewed Date, Review Title, Positive Feedback, Negative Feedback, and Review Score  

## Methodology

### Data Preprocessing
- Convert text to lowercase and tokenize  
- Remove punctuation and stop words  
- Apply lemmatization and convert emojis to text  

### Feature Identification
- Chunking and Affinity Propagation Clustering to generate exemplars  
- Hierarchical Clustering to refine groups  
- Feature Identification based on words closest to cluster centroids  

### Sentiment Estimation
- Apply VADER sentiment analysis on sentences mentioning identified features  
- Combine sentiment scores ranging from negative one to positive one to determine overall feedback  

### Machine Learning
- Classifiers: Decision Trees, Random Forest, LGBM, XGBoost, CatBoost  
- Validation: Nested cross validation for hyperparameter tuning and evaluation  
- Metric: F1 score used for performance comparison  
- Best Model: Random Forest with F1 score 0.9298  

### Interpretable Machine Learning
- SHAP used to explain Random Forest predictions, highlighting how each product feature impacts the rating  

### Customer Segmentation
- K Means Clustering on feature importance and satisfaction scores  
- Opportunity Score defined as Importance plus the maximum of Importance minus Satisfaction and zero  
- Highlights features critical to customers but underperforming  

## Results

- Random Forest achieved the highest F1 score of 0.9298  
- SHAP analysis revealed which hotel features most strongly influenced ratings  
- Customer Segmentation identified distinct groups and highlighted areas for improvement such as manager, bathroom, service, and price  

## Group Members

- Vishnu Vardhan (21CE3AI13)  
- Gowtham Chowdary (21CE10084)  
- Harvin Raj (21ME10090)
- Junius James (21ME31073) 
- Shiva Prasad (21ME31072)  
