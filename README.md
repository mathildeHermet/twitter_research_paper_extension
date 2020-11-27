# Tweeter usage prediction   
   
## Abstract   
The idea is to create a score that quantifies/measure, tweeter user activity. This score will come from a calcul based on the number of tweets the user posted, the number interaction with other users : number of direct message, number of mention, interaction with topics with hashtags number, urls number and likes.   
Then once we decided about how to compute the measure, this measure will be by week or by month, depending of the relevance of it.   
There are multiple goals : the first will be to have a tendency about how activity of tweeter user evolve along the month in a year : try to indentify a pattern of user activity depending on month in a year. That would be a kind of complementary study added to the circadian one realized in the paper. The second goal would be to create a model and try to see if we can predict if a user will remain active or not in the following years. This model will take into account followee, follower, likes, etc.   
## Research questions :   
Liste :   
- Can we predict the activity in the future of a user based on his data ?   
- Can we predict general behaviour of user depending on the month of the year ?    
## Proposed dataset   
We found the way researcher sampled and created the dataset based on twitter api very interesting. So we decided to keep it, but we plan on collecting more data, and maybe more recent one about same users id, through twitter api. We already created twitter developper account and we started experiments on it.   
We are planning to re use the following dataset used in the paper : EgoAlterProfiles.rar and EgoTimelines.rar
We are interested in created_at, mentions_ids, user_id, hashtags, urls, tweets_id, replyto_userid, retweeted_userid, retweet_count
We will use the python searchtweets library to interact with tweeter database and extract more information for the given user id : if they still exist, and also their use of private message and like.