## Introduction

Our project focuses on video games and predicting the amount of success that they have. We used the factors of genre, year of release, platform, publisher and rating scores/counts from critics/players in order to predict how good a game would be. We defined how good a game is as the sales all over the world.

## Importance

Gaming has already become a massive industry that not only competes with how much other industries such as movies and music, but even have more money put into the industry. Furthermore, if current trends continue as projected, they will grow even more as can be seen in the figure below.
![Image of Comparison to film and music](/images/comparison.PNG)

Although we can clearly see that gaming is a growing industry from the graph that is seen above, there are also other indicators that gaming will be an industry that continues to grow: in particualar, who plays games.
![Image of age groups that game](/images/ageGroups.PNG)

As can be seen from the above, it is very clear that gamers very much skew towards a younger audience. As with any industry, it is highly likely that people who are young and gaming, will continue to game and continue to contribute to the growth of the industry.

## Dataset

The dataset that we used was from [kaggle](https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings).

#### Characteristics of the data

There were a total of 16720 games in the dataset from 1980 to 2020.
The features include metrics such as genre, year of release, platform, publisher, scores by critics and users, as well as some that we did not use such as sales in various regions, rating, etc. (Note that only games that were released before 2016 had any sales numbers.)

![Image of data](/images/data.PNG)

We did not use this entire dataset but picked out effctive 6204 games for as train data set and 690 games as test data set.

## Approach

In this project, we will use supervised learning because we want to use features of games as an input to predict its rating as an output from the dataset above as the training dataset. 

We will use mutiple regression as the approach to find out the pattern and predict the values of the rating on additional unlabeled data because there are eight independent variables: Platform, Year_of_Release, Genre, Publisher, Critic_Score, Critic_Count, User_Score, User_Count, and we want to determine the degree to which these independent variales are influencing the rating, the dependent variable.

We will examine different regression models such as linear regression, ridge regression, lasso regression, elastic net regression and perform cross validation on them to find out the best model for our dataset.

Different than regression we did on our projects, we need to convert categorical variables into continuous variables before performing regressions because this is a real world dataset. This dataset contains categorical variables which can not be used in regression models because they require numerical values. We choose to use one-hot encoding to deal with this situation.

## Data Preprocessing

#### Data Cleaning
We deleted all data points with null or invalid values manually to avoid errors during data analysis.

#### One-hot Encoding
There are 4 CONTINUOUS VARIABLES in the dataset: Critic_Score, Critic_Count, User_Score, User_Count

There are 4 CATEGORICAL VARIABLES in the dataset: Platform, Year_of_Release, Genre, Publisher

We use one-hot encoding to convert categorical data into integer data because the regression model we intend to use in our project requires numerical values.

Using Genre as an example to perform one-hot encoding:

![Image of Genre Distribution](/images/genres.png)

We discover that there are 12 genres which is finite, and we will represent each genre as a binary vector. Each vector will have a length of 12 for the 12 possible values.

![Image of Genres One-Hot Encoding](/images/Genre_OHC.jpeg)

We perform One-Hot Encoding for all four categorical features as exemplified above with the Genre feature and convert them into binary values so that we can apply them to different regression models.

## Comparisons of Different Regression Models

## Cross Validations for Different Models

## Conclusion

![Image of result comparisons](/images/resultConparisons2.png)

Ridge regression was the best for this dataset out of linear regression, lasso regression, elastic net regression, and itself with an RMSE value of 1.267450 and a r^2 value of 0.354726. While this may be the optimal model for the regressions, it is still not a strong correlation by any means as the r^2 value, at best can only indicate a weak correlation between the factors that we had used as predictors and the scores that were given on Metacritic by fans and critics.

## Citations

Kirubi, Rush. “Video Game Sales with Ratings.” Kaggle, 30 Dec. 2016, https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings.

“The Video Games' Industry Is Bigger Than Hollywood.” LPE Esports, https://lpesports.com/e-sports-news/the-video-games-industry-is- bigger-than-hollywood.

“U.S. Average Age of Video Gamers 2019.” Statista, https://www.statista.com/statistics/189582/age-of-us-video-game-players-since-2010/.
