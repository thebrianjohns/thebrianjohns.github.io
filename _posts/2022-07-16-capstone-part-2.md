---
layout: post
title: "BrainStation Capstone Part 2"
subtitle: "Using Regression Models to Predict the Cap Hits of NHL Players"
date: 2022-07-16 12:00:00 -0400
background: '/img/contract.jpg'
---

Code for this part of my project can be found [HERE](https://github.com/thebrianjohns/hockeycaphits/blob/main/Brian%20Johns%20Capstone%20%232%20-%20Regression%20Modeling.ipynb)

This notebook starts with some Exploratory Data Analysis of cleaned data comprising of NHL salaries and statistics.  Utilizing the **seaborn** library, I visualized the distributions of each feature and the linear relationships between each feature and the target variable, an NHL player's Cap Hit.  As a result of the EDA, I used log and bimodal transformations in order to normalize the distributions of some of the data.  The data was then split into Train/Test sets in preparation for modeling.

I utilized the **scikit-learn** library in order to scale and then model the data.  I ran Linear Regression, Decision Tree, Random Forest and XGBoost models in order to make predictions about the NHL player's Cap Hits.  I measured R-squared, as well as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE), in order to evaluate the performance of each model.  In the end, the XGBoost Regressor was the highest performing model, with an R-Squared value of 67.9%, MAE of 0.94 and RMSE of 1.29.

Given the complexity of an XGBoost model, I used plot importance and **Shapley values** to interpret the results of the model.  Using these, there were five major predictors for a player's Cap Hit:

1. The player's age
2. The player's draft placement
3. The amount time on ice spent during a powerplay
4. The actual number of goals scored for their team while the player was on the ice
5. The number of *expected* goals scored for their team while the player was on the ice.

It came as no surprise that, based on the model, some of the players that had Cap Hits significantly lower than what the model predicted were outstanding young players that had not had their first contract extension, thus being limited to the rookie salary scale.  What was more of a surprise is that aging veterans, often older than 35 but still producing at a high level, were also consistently undervalued.  The biggest surprise was that the max value for a player's cap hit in the model was $9.5 million, nearly $3 million lower than the actual max cap hit.  This would seem to intimate that no player is worth the most expensive contracts currently in the league, even if their performance exceeds MVP levels.

To get a better sense of the differentiation between players, I decided to run Clustering models in an attempt to group players based on their statistics.  This can be found in Part 3 of my Capstone Project.