---
layout: post
title:  "Find a model that fits user activity to predict account future"
date:   2020-12-09 14:44:20 -0500
author: "Kali group"
feature: "predict_user_usage.png"
subtitle: "The second research question raised while working on the paper and its dataset is : 'Can we predict the future activity of an account baised on the user data ?'. We wanted to find if such a model exists and what parameters determines this prediction."
---
<div>
<h4>Abstract</h4>
<p>
The goal of this study is to predict the number of tweets a given user will have made in the present based on the data from the original paper, meaning data from 2014, and some data of 2020 such as its new followers’ count. We will try to use two model to perform the predictions : Ridge regression and Gradient boosting regression. 
</p>
<h4>Results</h4>
<p>
First of all, some cross-validation steps were performed. 
</p>
<p>
<img src="{{ site.baseurl}}/assets/images/CrossValRidge.png" class="half_width" />
<legend>Cross Validation for Ridge</legend>
<img src="{{ site.baseurl}}/assets/images/CrossValGBR.png" class="half_width" />
<legend>Cross Validation for Gradient Boosting</legend>
</p>
<p>
Those graphs seem to show, in addition to the best hyperparameters for both models, that Gradient Boosting will be outputting better predictions than Ridge.
</p>
<p>
<img src="{{ site.baseurl}}/assets/images/rrpred.png" class="half_width" />
<legend>Ridge prediction vs Actual data</legend>
<img src="{{ site.baseurl}}/assets/images/gbrpred.png" class="half_width" />
<legend>Gradient Boosting vs Actual data</legend>
</p>
<p>
<h4>Analysis</h4>
<p>
In reality, both these methods seem to give quite poor results. First of all, each model has a tendency to find some negative values, Gradient Boosting more than Ridge, which we know is impossible as no users could have a negative number of tweets. A reason this might occur is the existence of a reduction in the number of tweets for some user, in fact some user might have deleted their tweets for whatever reason, meaning that the number of tweets over time is going down. Then, we can clearly see a sort of constant at the start of each graph, with the one of Gradient Boosting being lower even though less visible than the one of Ridge, meaning that the models do not distinguish lower values very well.

All in all, it is unlikely to be able to predict the number of tweets a user will be making in 6 years based on some old data, because the number of tweets made by an account does not seem to correlate with the number of followers a user has.

Some idea to perform better would be to have a better history of the account, maybe on a year by year basis instead of a chunk of many year all in one category.
</p>
</div>