# Email Campaign Effectiveness Prediction
## Introduction
The objective of this machine learning (ML) project is to develop a model that effectively analyzes and tracks emails sent as part of Gmail-based email marketing strategies employed by small to medium-sized business owners. The goal is to classify emails based on their characteristics and monitor their recipients' engagement, distinguishing between emails that are ignored, read, or acknowledged.

## Exploratory Data Analysis (EDA)
### Email Status Distribution
* A majority of emails in the dataset (80.4%) were ignored, indicating a need for improved engagement strategies.
* A smaller proportion of emails (16.1%) were read, showing room for enhancing reader engagement.
* Only a small fraction of emails (3.5%) were acknowledged, suggesting that optimizing email content is crucial for eliciting responses.

  
![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/035c56eb-9673-4b8a-b348-0186adadd684)


### Comparison of Email Types Across Email Status
* Marketing emails were largely ignored, emphasizing the challenge of capturing recipients' attention.
* Important updates/notice emails also faced significant ignorance.
* Both marketing and important updates/notice emails had moderate reads.
* Acknowledged emails were a minority for both email types.

![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/3a48312a-bf45-4473-a269-3267b2d8c324)


### Average Email Word Count by Email Source Type
* Sales & marketing emails and important admin emails had higher average word counts, indicating more detailed content.
* Important admin emails had slightly higher word counts than sales & marketing emails.
* Sales & marketing emails appeared to focus on concise messaging.

![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/a82835a0-6491-490b-98be-ed2015d7a1d1)


### Average Word Count across Subject Hotness Scores
* Emails with higher subject hotness scores had shorter word counts, suggesting brevity in engaging content.
* Emails with lower subject hotness scores tended to be longer.

![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/46937db3-7c13-4a15-a7d5-245874efb94e)

  
### Subject Hotness Score Distribution
* The distribution of subject hotness scores was right-skewed, indicating that most subjects were not highly engaging.
* There was a peak near a score of 0.25, indicating a lack of highly engaging subjects.
* Higher hotness scores were rare, suggesting few highly compelling subjects.

![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/2ba2e890-4140-43f9-8a31-d2b0ef129be2)


### Average Word Count vs. Total Links
* As word count increased, the average number of links also tended to increase, peaking at around 1000 words.

![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/359145c9-3346-421d-931b-e0ad3279448b)

  
## Feature Engineering
* Created a 'Links+Images' column by combining 'Total_Links' and 'Total_Images.'
* Dropped 'Time_Email_sent_Category' and 'Email ID' due to low correlation with the target variable ('Email Status').
* Utilized SMOTE (Synthetic Minority Over-sampling Technique) to handle the imbalanced dataset by generating synthetic minority class samples.

## Model Building
Three models were built:

* **Logistic Regression:** Average F1 score of **0.51** for all three categories.
* **Naive Bayes:** Average F1 score of **0.45** for all three categories.
* **Random Forest:** Average F1 score of **0.85** for all three categories.
  
Comparing F1 scores, the **Random Forest Classifier** outperforms other models with significantly higher scores (0.86, 0.79, and 0.90 for classes 0, 1, and 2, respectively).

![image](https://github.com/mohd-arham-islam/Email-Campaign-Effectiveness/assets/111959286/050d3dc4-876e-4515-8b57-11482d89213b)


## Conclusion
In conclusion, the Random Forest Classifier emerged as the most effective model for classifying emails in this Gmail-based email marketing project. Its superior precision, recall, F1 score, and accuracy provide valuable insights for businesses to refine their email marketing strategies and optimize engagement rates.

The Random Forest Classifier's strength lies in its capability to capture complex relationships within the email dataset and handle diverse email characteristics, making it an ideal choice for this project. Its successful implementation empowers small to medium-sized business owners to gain actionable insights and improve their email marketing campaigns.
