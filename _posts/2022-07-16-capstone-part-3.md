---
layout: post
title: "BrainStation Capstone Part 3"
subtitle: "Clustering NHL Players Based on Basic & Advanced Statistics"
date: 2022-07-16 11:00:00 -0400
background: '/img/helmets.jpg'
---

Code for the third, and final, part of my project can be found [HERE](https://github.com/thebrianjohns/hockeycaphits/blob/main/Brian%20Johns%20Capstone%20%233%20-%20Clustering%20Models.ipynb)

With Exploratory Data Analysis and Regression modeling having been completed, I endeavored to utilize K-Means Clustering in hopes of grouping NHL players based on their on-ice performance statistics.

In preparation for this, I used sevearl parts of the **scikit-learn** library to evaluate how the data may cluster.  First, I visualized the data using Principal Component Analysis and T-distributed Stochastic Neighbor Embedding (t-SNE) and plotted the data using **seaborn**.  I then calculated the silhouette score and inertia for 10 and fewer clusters to see what would be the best number for this dataset.  The best silhouette score was only 0.19, so while there may not be a lot of separation in the data, I felt that there may still be some insights that could be gained by clustering the data and evaluating the results.

I first ran the clustering model across all players into 4 groups.  The results did not reveal many insights as the players were roughly divided by overall performance: good (but not necssarily great), average, below average and fringe NHL players.  I then did separate clustering for Forwards and Defencemen.  While the silhouette scores were still relatively low, this yielded more insightful results.

Dividing defencemen into 4 groups created more definitive 'roles' on the ice: Stars, Offensive Producers, 'Stay-At-Home' Defencemen and Fringe NHLers.  Dividing forwards into 6 groups produced more illuminating results: Stars, purely offensive producers, purely defensive forwards, secondary defensive forwards, fringe NHLers and Enforcers (players that essentiall just fight).

Plotting players by their cluster within each team, and in particular the Stanley Cup winning teams, suggest that a team should prioritize improving the depth of their team over signing expensive star players that limit the teams ability to acquire more talent.  An NHL team should be cautious if they plan to act on these findings.  In the future, clustering methods may be more valuable by limiting the number of variables that a team finds most valuable or with the additional input of player tracking data.

A recap of my entire BrainStation Capstone Project can be found [HERE](https://github.com/thebrianjohns/hockeycaphits/blob/main/Brian%20Johns%20Capstone%20%234%20-%20Findings.ipynb).

The final draft of the business report, including a summary of my findings and visualizations to support them, can be found <a href="https://thebrianjohns.github.io/Brian%20Johns%20Capstone%20-%20Report.pdf" target="_blank">HERE</a>