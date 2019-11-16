## Introduction

Our project focuses on video games and predicting the amount of success that they have. We used the factors of genre, year of release, platform, publisher and rating scores/counts from critic/players in order to predict how good a game would be. We defined how good a game is as the sales on the global area.
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

We did not use this entire dataset and arbitrarily picked out 6204 games for our training set and 690 games for our test set. the breakdown of the genres of training set were as follows.

![Image of genres](/images/genres.png)

## Preprocessing

## Comparisons of Different Regression Models

## Cross Validations for Different Models

## Conclusion

Ridge regression was the best for this dataset out of linear regression, lasso regression, elastic net regression, and itself with an RMSE value of 1.429764 and a r^2 value of 0.305834. While this may be the optimal model for the regressions, it is still not a strong correlation by any means as the r^2 value, at best can only indicate a weak correlation between the factors that we had used as predictors and the scores that were given on Metacritic by fans and critics.

## Citations

Kirubi, Rush. “Video Game Sales with Ratings.” Kaggle, 30 Dec. 2016, https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings.

“The Video Games' Industry Is Bigger Than Hollywood.” LPE Esports, https://lpesports.com/e-sports-news/the-video-games-industry-is- bigger-than-hollywood.

“U.S. Average Age of Video Gamers 2019.” Statista, https://www.statista.com/statistics/189582/age-of-us-video-game-players-since-2010/.
