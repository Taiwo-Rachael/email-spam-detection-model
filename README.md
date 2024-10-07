# 🚀✉️ Email Spam Detection Model: Filtering the Junk, One Email at a Time!
## 📊 📉 Introduction
In today's digital age, inboxes are constantly under siege by unwanted emails, from fake promotions to phishing scams. Sometimes, really important emails end up in the spam folder, which could at times be really frustrating, or even lead to missing important deadlines. This project is designed to combat that flood of junk by implementing an Email Spam Detection Model that leverages natural language processing (NLP) techniques and machine learning algorithms to distinguish between ham (legitimate emails) and spam (unwanted emails). This model will help to ensure inboxes are kept clean and important emails do not end up in the spam folder. 

By analyzing key features such as word frequency, email length, and more, this model learns from patterns in email content, detecting common spam triggers and filtering them out with precision. Let's dive in!

## 📊 📈  The Dataset
The dataset used for this project consisted of five columns. The main columns being:  

**v1 (Status):** Indicating whether each email is classified as spam or ham.    
**v2 (Emails):** Containing the email texts.  

Additionally, there were three unnamed columns with over 90% missing values, which were removed during the data cleaning process. The dataset originally comprised 5,572 emails before any cleaning was performed. You can checkout the initial dataset [here](https://github.com/Taiwo-Rachael/email-spam-detection-model/blob/main/spam.csv).

## 🧹🧹 Data Cleaning and Feature Engineering
Getting the dataset clean and ready for analysis involved a number of processes, including dropping off the unnamed columns, removing 403 duplicated entries and renaming the v1 column as 'Label' and v2 as 'Email' for clarity. After cleaning, the dataset contained 5169 rows and 2 columns. To gain deeper insights into the nature and characteristics of spam and ham emails, two new columns, 'Email Length' and 'Length of Words' were created. The email length was generated by applying the 'len' function to each mail while the length of words was generated by applying the 'word_tokenize' and 'len' function to each mail.

##  🔍 🔍 Exploratory Data Analysis (EDA)
