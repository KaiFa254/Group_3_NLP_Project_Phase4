![Apple and Google](https://github.com/user-attachments/assets/350460c9-cdad-4724-9fae-5c120657dd29)

Source by https://uzalendonews.co.ke/google-retains-chrome-and-apple-partnership-but-must-share-data-in-landmark-antitrust-decision/

## Project Structure and Navigation

- *`README.md` — Project documentation*
- *`NLP.ipynb`  — Jupyter notebook for analysis*
- *`Data/` — Dataset files*
- *`Presentation/` — Project summary slides PDF*
- *`Links/` — Deployment/Tableau and Source Link*

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
### Real-Time Brand Reputation Dashboard
Observation: The tuned Logistic Regression model achieves ~87% accuracy and can classify tweets in near real time.
Recommendation: Deploy the model as a live dashboard for Marketing and Communication teams to track hourly/daily sentiment shifts. Trend charts can provide early warnings for product issues (e.g., spikes in negative tweets). Integration with CRM will allow logging of dissatisfied customers for structured follow-up.
### Product Improvement from Feedback Themes
Observation: Negative tweets frequently mention failures, crashes, and usability frustrations. Positive tweets emphasize features, freebies, smart design, and enjoyable experiences.
Recommendation: Product Teams should analyze negative feedback for recurring pain points and prioritize fixes (e.g., performance issues). Positive themes should guide new feature development, such as offering more free trials or reward bundles that align with what customers value most.
### Use Sentiment Insights for Proactive Customer Engagement
Observation: Negative tweets often include words like “fail,” “hate,” “crash,” “wont,” “long,” and “headache.”
Recommendation: Customer Support Teams should monitor these signals in real time and proactively reach out to dissatisfied users. Automated alerts should be set up for spikes in negative sentiment, especially during product launches or updates.
### Leverage Positive Sentiment for Marketing
Observation: Positive tweets contain words such as “cool,” “great,” “free,” “awesome,” and “winning.”
Recommendation: Marketing Teams should amplify these organic positive posts through retweets, testimonials, and influencer engagement. Launching hashtag campaigns tied to new product releases can also help encourage more positive buzz and word-of-mouth.
Address Class Imbalance in Feedback
Observation: Neutral tweets are the majority (~60%), and Negative tweets are underrepresented (~16%). The model struggles more with detecting Negative sentiment (recall = 0.56).
Recommendation: Encourage customers to provide clearer feedback through surveys, polls, or structured channels.

Enhance monitoring by combining Twitter with other sources (customer forums, Reddit, app reviews) to capture more diverse negative cases.

Invest in more labeled training data for negative sentiment to strengthen detection.

## 9. Dashboards 
<img width="1280" height="505" alt="image" src="https://github.com/user-attachments/assets/56d19c85-f8b4-49f0-a367-b371a4ea1754" />
Aspect                       | Observation                                                                                   

i. Volume Leader             - Most tweets are either not directed at any brand/product or are uncategorized ("Null"). 

ii. Emotion Distribution     - Most tweets show *positive emotion* or *no emotion*. Very few express negative emotion.

iii. Popular Targets         - iPad and Apple receive the most attention in emotional tweets.                                  
iv. Low Sentiment Visibility - "I can’t tell" has minimal counts – indicating clear labeling for most tweets.

Link to Tableau: https://public.tableau.com/views/Group3NLPTableauDashboard/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
   
## 10. Links
Link to the model: https://group-3-project-app-46ae69b19de0.herokuapp.com/
