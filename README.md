# 🚀✉️ Email Spam Detection Model: Filtering the Junk, One Email at a Time!
## 📊 📉 Introduction
In today's digital age, inboxes are constantly under siege by unwanted emails, from fake promotions to phishing scams. Sometimes, really important emails end up in the spam folder, which could at times be very frustrating, or even lead to missing important deadlines. It's usually not a funny feeling when you go through your spam folder only to find that email you have been waiting for sitting right there! especially if it has caused you to miss out on an important opportunity. This project is designed to combat that flood of junk by training an Email Spam Detection Model that leverages natural language processing (NLP) techniques and machine learning algorithms to distinguish between ham (legitimate emails) and spam (unwanted emails). This model will help to ensure inboxes are kept clean and important emails do not end up in the spam folder. 

By analyzing key features such as word frequency, email length, and more, this model learns from patterns in email content, detecting common spam triggers and filtering them out with precision. In the [Jupyter Notebook](https://github.com/Taiwo-Rachael/email-spam-detection-model/blob/main/Email_Spam_Detection_Model.ipynb), you'll be able to see my full coding process, showing how I carried out the following steps for this project:

1. Data Cleaning  
2. Feature Engineering  
3. Exploratory Data Analysis
4. Email Preprocessing
5. Word Cloud Generation
6. Encoding and Vectorization
7. Model Selection and Training
8. Model Evaluation and Demonstration

## 🧹🧹 Data Cleaning and Feature Engineering
Getting the dataset clean and ready for analysis involved a number of processes, including dropping off unnamed columns which also contained over 90% null values, removing 403 duplicated entries and renaming the v1 columns for clarity. After cleaning, the dataset contained 5169 rows and 2 columns. To gain deeper insights into the nature and characteristics of spam and ham emails, two new columns, 'Email Length' and 'Length of Words' were created. The email length was generated by applying the 'len' function to each mail while the length of words was generated by applying the 'word_tokenize' and 'len' function to each mail.

##  🔍 🔍 Exploratory Data Analysis (EDA)
Taking a deep dive into the dataset revealed some interesting insights, including the fact that spam emails tend to be longer than ham emails, and also contain more words. A correlation analysis however, revealed that the length of words and email length in themselves are not strong enough factors to determine whether or not an email will be classified as either spam or ham, with correlation coefficients of 0.26 and 0.38 respectively with the label.

## ✉️🧹 Email Preprocessing
In order to get the emails ready for further analysis and modeling, it was necessary to pass the individual mails through a cleaning process including removing punctuations and special characters, tokenization (a NLP technique that splits the raw text into small chunks of words called tokens), Part of Speech (POS) tagging, stop words removal and lemmatization (a NLP technique that breaks a word down to its root meaning or base form to identify similarities). I did this by defining a 'clean' function to carry out all these processes in a single run. 

## ☁️ ☁️ Word Cloud
After preprocessing the emails, they were ready for the  next steps. At this point, the goal was to find out what words were most common in the spam emails. To achieve this, a word cloud was generated. The size of the words in the cloud is an indication of the frequency. The most common words appear much larger than the others. The word 'call' tops the list here, appearing about 300 times. The frequency of the other words can be seen in the bar chart. The presence of these words in an email will most definitely trigger its classification as spam by the model.

<p align="left">
  <img src="https://github.com/user-attachments/assets/dea6b4e5-57f9-45ef-a5fb-fe09196e1ef6" width="800"/>
</p>

<p align="left">
  <img src="https://github.com/user-attachments/assets/046c6a79-5083-47dd-90ad-13d0c440112e" width="800"/>
</p>

## 🤖🤖 Modeling
**Encoding and Vectorization**
To get the data ready for the model training, the next thing I had to do was to convert the emails and their labels into numerical forms that the model would be able to work with, as Machine Learning models only work with numerical data. For the emails, they were converted into vectors using the Count Vectorizer while the labels were encoded using the Label Encoder.

**Model Training and Evaluation**
Several classification models including the logistic regression classifier, SVC, random forest classifier and XGBoost classifier were selected and trained in order to determine the best performing one. After comparing the results of the models and tuning hyperparameters, the **Logistic Regression Classifier** had the best performance and was used for classification. This model achieved a precision of 98% for ham emails and 99% for spam emails, demonstrating its strong ability to distinguish between spam and legitimate emails. Additionally, with a high recall percentage of 99.89% for ham emails, it ensures minimal misclassification of genuine emails. Ensuring that important emails don't end up in the spam box.

## Conclusion 
The model demonstrates effectiveness in applying machine learning algorithms to classify emails as either spam or ham.  With the balance of high recall and precision recorded, the model achieves the primary objective—keeping the inbox free of unwanted emails while ensuring that no essential communications are lost in the spam folder. This reliable performance makes the model well-suited for practical applications and further improvements.








