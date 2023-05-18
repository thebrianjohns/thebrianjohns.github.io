---
layout: post
title: "Sentiment Analysis of Dallas Mavericks Tweets Part 2"
subtitle: "Feature Engineering and NLP for Dallas Mavericks Tweets"
date: 2023-05-18 13:00:00 -0400
background: '/img/mavstweets/shot.jpg'
---

Code for this project can be found [HERE](https://github.com/thebrianjohns/mavstweets/blob/main/Mavs%20NLP%20%232%20-%20Feature%20Engineering.ipynb)

This notebook starts with adding features to the dataset to utilize as much data as possible from the raw data into analysis, but also adding additional information that I thought would help in creating a more predictive model.  Namely, I added the Dallas Mavericks game schedule, whether they won or not, and their winning percentage at the time of the tweet to the dataset in hopes that the on-court performance would be predictive of the fans' sentiment in their tweets.

Once my feature engineering was complete, I then conducted Natural Language Processing (NLP) on the dataset.  I chose to use **TFIDF** Vectorization on the dataset.  In doing so, I used the **NLTK** library to stem and lemmitize the words/tokens in order to optimize the NLP process that I felt would be most predictive.  

With NLP completed, the dataset was now ready for modelling.  In Part 3 of this project, I perform additional exploratory data analysis on the fully prepared dataset, as well as Logistic Regression and Naive Bayes modelling to predict the Sentiment of the tweets.