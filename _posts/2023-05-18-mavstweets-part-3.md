---
layout: post
title: "Sentiment Analysis of Dallas Mavericks Tweets Part 3"
subtitle: "Classification Modelling and Summary For Tweets Mentioning the Dallas Mavericks"
date: 2023-05-18 13:00:00 -0400
background: '/img/mavstweets/fullcourt.jpg'
---

Code for this project can be found [HERE](https://github.com/thebrianjohns/mavstweets/blob/main/Mavs%20NLP%20%233%20-%20Classification%20Modeling.ipynb)

In preparation for modelling, I conducted additional exploratory data analysis on the fully prepared dataset.  Based off of this, in addition to the NLP conducted, I felt that the frequency a user tweeted and whether the Mavericks won or lost could be predictive factors for Sentiment.

I then utilized the **Sci-Kit Learn** library to conduct multi-nomial classification modelling for the dataset.  In the end, my most predictive model required:
- Utilizing **SMOTE** to balance the data
- Scaling the data, with Standard Scaling being the highest performing
- Logistic Regression over Naive Bayes

The 'saga' solver performed the best, but given the computing challenges and the size of the data, I chose the Logistic Regression model using a 'lfgbs' solver to do my final scoring on the testing data.

The Final Summary for this project can be found [HERE](https://github.com/thebrianjohns/mavstweets/blob/main/Mavs%20NLP%20%234%20-%20Summary.ipynb)

My final Logistic Regression Model had a 83.45% Overall Accuracy.  The user frequency, location of the tweets and whether the Mavericks won or lost were all highly predictive factors for Sentiment, in addition to some key tokens identified through NLP such as tweets with explitives and synonyms for 'bad'.

Within this accuracy, the model was best at distinguishing the difference between Neutral tweets and those with Positive or Negative Sentiment (AUC = 0.94) whereas it was the lowest performing in identifying Negative tweets specifically (AUC = 0.88).

Using a model such as this could help the Mavericks identify specific communities to target campaigns and ticket sales and give a first glance of fan's issues and help the Mavericks provide a better fan experience.