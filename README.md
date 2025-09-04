![Apple and Google](https://github.com/user-attachments/assets/350460c9-cdad-4724-9fae-5c120657dd29)

Source by https://uzalendonews.co.ke/google-retains-chrome-and-apple-partnership-but-must-share-data-in-landmark-antitrust-decision/
# Sentiment Analysis of Tweets on Apple and Google Products

## 1. Project Overview
This project analyzes public sentiment about Apple and Google products using tweets. The goal is to classify opinions into **Positive**, **Negative**, or **Neutral** categories and identify trends that can guide product and marketing strategies.

## 2. Business Understanding
Understanding customer sentiment helps businesses:
- Detect product strengths and weaknesses.
- Measure the impact of marketing campaigns.
- Respond proactively to negative feedback.

Apple and Google are leading tech companies with strong online presence, making them ideal candidates for sentiment analysis.

## 3. Dataset Overview
- **Source:** CrowdFlower (now Figure Eight)
- **Size:** ~9,000 labeled tweets
- **Target variable:** Sentiment (Positive, Negative, Neutral)
- **Issue:** Slight class imbalance requiring oversampling

## 4. Data Preparation
Key preprocessing steps:
- Removed punctuation, special characters, and stop words.
- Converted text to lowercase and lemmatized tokens.
- Encoded sentiment labels numerically.
- Extracted features using **TF-IDF vectorization**.
- Handled class imbalance using **SMOTE oversampling**.

## 5. Modeling Approach
Several models were evaluated:
- Logistic Regression  
- Random Forest  
- Gradient Boosting  
- AdaBoost  
- XGBoost  
- Naive Bayes  

Hyperparameter tuning was performed using **RandomizedSearchCV** to improve accuracy.

## 6. Results
- **Best Model:** Logistic Regression  
- **Accuracy:** ~87% on validation data  
- **Key findings:**  
  - Positive tweets often contained words like *love*, *amazing*, *great*.  
  - Negative tweets often contained words like *bad*, *worst*, *disappointing*.  

## 7. Insights
- Logistic Regression outperformed more complex models, showing that sentiment classification benefits from clean features over complex architectures.
- Certain keywords are strong indicators of sentiment and can be tracked for brand monitoring.

## 8. Recommendations


## 9. Dashboards 
<img width="1280" height="505" alt="image" src="https://github.com/user-attachments/assets/56d19c85-f8b4-49f0-a367-b371a4ea1754" />
Aspect                       | Observation                                                                                   

i. Volume Leader             - Most tweets are either not directed at any brand/product or are uncategorized ("Null"). 

ii. Emotion Distribution     - Most tweets show *positive emotion* or *no emotion*. Very few express negative emotion.

iii. Popular Targets         - iPad and Apple receive the most attention in emotional tweets.                                  
iv. Low Sentiment Visibility - "I can’t tell" has minimal counts – indicating clear labeling for most tweets.

Link to Tableau: https://public.tableau.com/views/Group3NLPTableauDashboard/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
   
## 10. Model Deployment
Link to the model: https://group-3-project-app-46ae69b19de0.herokuapp.com/
