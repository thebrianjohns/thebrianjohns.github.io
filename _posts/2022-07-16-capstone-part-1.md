---
layout: post
title: "BrainStation Capstone Part 1"
subtitle: "Acquiring & Cleaning Data for NHL Salaries and Statistics"
date: 2022-07-16 13:00:00 -0400
background: '/img/rink.jpg'
---

Code for this project can be found [HERE](https://github.com/thebrianjohns/hockeycaphits/blob/main/Brian%20Johns%20Capstone%20%231%20-%20Data%20Cleaning.ipynb)

My first notebook introduces the problem space for my Capstone project by giving some financial background of the NHL and asking my business question: **How can we predict and evaluate the Cap Hits of NHL players using their basic and advanced statistics?**

In order to answer this, I acquired data from two sources:
1. [<u>CapFriendly</u>](https://www.capfriendly.com/) for NHL financial information, such as salaries and cap hits.
2. [<u>Evolving Hockey</u>](https://evolving-hockey.com/) for on-ice performance statistics for NHL players.

I decided to focus on just the last ten years of data, as the financial information was the most reliable and relevant in order to make short-term predictions.

To acquire the financial information, I used **Beautiful Soup** in order to webscrape the data.  Using my premium membership for Evolving Hockey, I was able to download the hockey statistics in 8 separate csv's and combine them using **Glob**.  All of the data was then merged and cleaned utilizing the **Pandas** library.

Cleaning the data to be ready for modeling presented some unique challenges.  In order to combine the data required merging them together based on the players' names.  However, numerous names were formatted differently, such as with accents, use of initials or shortening the first name.  This required additional research and hard coding using the .loc() method in order to maximize the amount of data that was usable.

In the end, I had 6226 unique player/years (ie. 10 rows for Sidney Crosby, one for each season) with 146 features, the vast majority of which being numerical hockey statistics, with a handful of categorical features, such as the player position and handedness.  The regression modeling of this data is conducted in Part 2 of my project.