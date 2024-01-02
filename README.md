# Useful-prediction-of-review-from-Yelp-dataset

## Problem Defined:
The problem is to predict the usefulness of reviews on Yelp, a business review website. The dataset is assumed to have three types of features representing the fame of the business, the objective validity of the review, and the centrality of the reviewer in the network.

## Data Preparation:
Considering the integrity of the data, I chose the Yelp public dataset. The dataset includes 216,902 reviews, 5,852 business information, and 91,700 user information from 2008 to 2018.

## Data Process:
- Merge the 3 tables into a single table with 22 features.
- Preprocess the reviews and extract 50 topics using Latent Dirichlet Allocation (LDA).
- Feature Engineering:
    - Based on reviews: the length ratio of the review after removing useless characters, the number and ratio of topic words and categories words (restaurant categories, assuming valid words exist), and the length of the review time etc.
    - Based on reviewers: the duration of the reviewer’s use of Yelp, The average usefulness of the reviewer’s reviews, Whether the reviewer is a repeat customer.
    - Category features: Statistical features based on the 'useful' field.
- Feature Augmentation: Cross-processing of fields highly related to usefulness
- Finally, I got 190 variables

## Model Training and Evaluation:
- Linear regression model： Mean Absolute Error (MAE) of 0.61 and a Mean Squared Error (MSE) of 1.89.
- Applied ensemble models XGBoost and LightGBM:optimizing the model results through random grid search parameter tuning, they performed best with an MSE of 0.23 and an MAE of 0.07.
- However, stacking the two models did not significantly improve performance.

## Data Analysis:
- Ablation experiment: Further explored how the newly constructed features and each table contribute to predicting the usefulness of reviews.

## Conclusion:
- Businesses should pay attention to influencers on the network.
- Consumers sometimes overlook recent reviews that are more objectively useful.

