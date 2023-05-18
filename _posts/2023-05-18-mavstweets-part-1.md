---
layout: post
title: "Sentiment Analysis of Dallas Mavericks Tweets Part 1"
subtitle: "Cleaning Data for Tweets Mentioning the Dallas Mavericks"
date: 2023-05-18 13:00:00 -0400
background: '/img/mavstweets/emptycourt.jpg'
---

Code for this project can be found [HERE](https://github.com/thebrianjohns/mavstweets/blob/main/Mavs%20NLP%20%231%20-%20Data%20Cleaning%20%26%20EDA.ipynb)

My first notebook introduces the problem space for this project by asking the question: **How can we predict the sentiment of tweets directed at a professional sports team?**.  In this case, I am using tweets that mention the key phrase 'Dallas Mavericks'.

In order to answer this, I acquired data that was collected by Alex Huggler by gathering all tweets that mentioned 'Dallas Mavericks' during the 2021-22 basketball season.  The data is hosted on Kaggle and can be found [HERE](https://www.kaggle.com/datasets/alexhuggler/dallas-mavericks-twitter-data-for-20212022-games) and hosted on Kaggle.

I utilized the **Pandas** library in order to organize and manipulate the data.  In doing so, I:
- Focused on English Language Tweets
- Removed Emojis from the Tweets
- Utilized **VADER** to get Sentiment Scores for each tweet
- Used the Sentiment Scores to establish whether a tweet was Positive, Negative or Neutral.  This classification became the target variable for my modelling.

The end result of this was a somewhat imbalanced dataset, where approximately 40% of the tweets were Positive, 40% were Neutral but only 20% were Negative.

With the dataset cleaned, the next step was to use Natural Language Processing and Feature Engineering to ensure the dataset was ready for modelling and this was conducted in Part 2 of this project.