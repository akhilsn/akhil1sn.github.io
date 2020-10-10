---
layout: project
type: project
image: images/textClasssification.jpg
title: BBC articles fulltext and category
permalink: projects/bbcnewsclassification
# All dates must be YYYY-MM-DD format!
date: 2020-04-12
labels:
  - Naive Bayes
  - Logistic Regression
summary: Built a News Headline Classification model (Tech, Business, Sports, Entertainment, Politics) using Naive Bayes and Logistic Regression modeling performing well on the performance metrics.
---

Here I have used the BBC headline news text, labeled in 5 categories, i.e., 'Tech', 'Sports', 'Business', 'Entertainment', and 'Politics', and then trained models with Logistic Regression and Naive Bayes.

This is a Kaggle problem, and the dataset for the same can be taken from my github or the kaggle website.
Source: <a href="https://www.kaggle.com/yufengdev/bbc-fulltext-and-category">kaggle-dataset</a>
<br><br>
Dataset contains labeled BBC articles with fulltext (Title, body) and category of over 2 thousand BBC full text articles.
<br><br>
***The results obtained are very good for the dataset used.***<br>
> For Logistic Regression model, the model test accuracy is 98.35%<br>
> For Naive Bayes model, the model test accuracy is a little higher at 98.65%<br><br>

For the complete code please refer
Source: <a href="https://github.com/akhilsn/Kaggle-Projects/tree/master/BBC%20Text%20News%20Classification"><i class="large github icon "></i>akhilsn/BBC Text News Classification</a>

Finally I have used some random 'out of the dataset' headlines to test whether the model correctly classifies them into expected label class or not. And the results are extremely impressive!!
<br><br>Below I have used some random news headlines from the web, and using the model vuilt done the respective news classification.<br>

***Headline: FIR against Delhi Minorities Commission chairman for inflammatory content on social media***<br><br>
POLITICS
<br><br><br><br>

***Headline: Need to restart economy but with caution: Yogi Adityanath at E-Agenda AajTak***<br><br>
BUSINESS
<br><br><br><br>

***Headline: 2 doctors attacked in Andhra Pradesh Vijayawada***<br><br>
POLITICS
<br><br><br><br>

***Headline: If I bat for an hour, you’ll see a big one: How Dravid spelt doom for Pak***<br><br>
SPORTS
<br><br><br><br>

***Headline: Benedict Cumberbatch returns as Doctor Strange in new Spider-Man film***<br><br>
ENTERTAINMENT
<br><br><br><br>

***Headline: Portugal Train To Face France In The Nations League***<br><br>
SPORTS
<br><br><br><br>

***Headline: Taiwanese Apple Contract Manufacturers To Invest 900 Million USD In India: Report***<br><br>
BUSINESS
