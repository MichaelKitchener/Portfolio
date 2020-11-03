# Portfolio
This site is designed to provide a brief overview of some projects I have created. 

## Predicting Political Ideology of Reddit Users (WIP - LINK NOT UPLOADED)

I created a dataset of reddit users, their political ideology as per the political compass model (https://www.politicalcompass.org/) and a record of the frequency with which they interact with a range of subreddits via both comments and posts. This was done using PRAW (reddit API wrapper for Python) and pandas. 

(put in shape of dataset, mention it could've been longer)

Then, using scikit-learn, I created a classification pipeline that scales the data appropriately, reduces the dimensions using PCA and, finally, predicts various ideological binaries (is authoritarian vs is not authoritarian, is libertarian right vs is not libertarian right, etc.) using regularized logistic regresssion (ridge). Optimal parameters were estimated via a grid search.

Lastly, I created a tool that allows you to put in any user's username and predict their status for variou

The five primary ideologies features on the political compass and the accuracy for which my model could classify them (using cross validation with 5 folds) were:
* Authoritarian left: 95.3% 
* Authoritarian right: 91.9%  
* Libertarian left: 83.7%      
* Libertarian right: 80.5% 
* Centrist: 89.0% 

These results sound good but there are a few things to keep in mind. 1) The ammount of positive samples for each category is not particularly large. 2) The sample is almost certainly biased since people who publically flair their comments with their political ideology are no doubt more likely to express their political identity in otherways that are refelected in their digital footprint.

Nevertheless, it has been an interesting project and I plan to see how well these models perform for randomly selected users who do not necessarily post (this will require a survey of sorts). 

