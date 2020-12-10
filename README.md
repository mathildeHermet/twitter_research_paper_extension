# Twitter usage prediction   
   
## Abstract   
The idea is to use our data to predict twitter user activity (how much will he post on Twitter). This prediction will use the multiple features we have access to like the number of tweets the user posts, the number of interactions with other users : number of mention, interaction with topics with hashtags number, urls number and likes.
There are 2 main goals : the first will be to have a tendency about how activity of Twitter users evolves along the months in a year : try to indentify a pattern of user activity depending on month in a year. That would be a kind of complementary study added to the circadian one realized in the paper.   The second goal would be to create a model to predict if a user will remain active or not in the following years. This model will take into account, number of tweets, followee, follower, likes, etc.   
## Research questions :   
- Can we predict general behaviour of users depending on the month of the year (do people tweet more in December than June) ?
- Can we predict the activity in the future of a user based on his current data ?   
- Typically, how much tweets will he post? Will he delete his account ?   
## Proposed dataset   
We decided to keep the dataset used in the research paper as our main dataset because it was created in the most random way according to the researcher, meaning it's a good representation of the twitter community. Furthermore, this dataset has only user which were active in the last 6 months (from when it was created), which saves us time as we only want active user for our research. However we plan on collecting more recent data about our users through the Twitter api. We already created Twitter developper accounts to see how we could get this new data.
We are planning to re use the following dataset used in the paper : EgoAlterProfiles.rar and EgoTimelines.rar
We are interested in created_at, mentions_ids, user_id, hashtags, urls, tweets_id, replyto_userid, retweeted_userid, retweet_count
We will use the python searchtweets, tweepy libraries to interact with the Twitter database and extract more information for the given user id : if they still exist, how much tweets they have now etc...
## Methods
**Data collection** : We will use the Twitter API, for which we already got credentials, to extract some more data about our egos and will merge those informations with the one we already have in the two datasets mentioned above.

**Data analysis** : We want to understand how the users' activity works, to do so, we will use the timeline dataset and analyse the dates at which users are tweeting but also when they are interacting on the platform on a more general scale (to see if it's feasible).

**Predictions** : We will train a learning algorithm from `sklearn` such as `GradientBoostingRegressor` to try to predict a specific user's activity in the future and to predict the general behavior of users depending on the month as mentioned in Research questions. We will train our model using the data found during our data analysis step.
## Proposed timeline
**Week 1** : Gathering all the data we need from the Twitter API, and merging all the data needed to begin our analysis. Visualizing our data by doing graphs about the behaviour of users depending on the month and the mean time between tweets.

**Week 2** : Finishing our data analysis and starting to train the model using the data found on week 1.

**Week 3** : Finishing the model training, meaning that we should try some new models and see if they fit more with our tasks.
## Organization within the team

We will mostly work together on every part of the project as we all want to learn the most of it.

## Dataset    
   
Here are the links to the two new datasets generated using tweepy, a python librairie to use Twitter Api :
* [list of account that does not longer exist](https://drive.google.com/file/d/1hNJNKgmvu6Ar8sY-YGYmIbi6IPvcJQKv/view?usp=sharing)
* [recent data of user present in ego_timelines database](https://drive.google.com/file/d/1IGnrCDAH8RnpZm-6HU3jg8nqiANOSBw_/view?usp=sharing)
