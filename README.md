
# IPL Prediction Tool

Cricket is a wonderful game with not so complex rules, TLDR about cricket is a ball is thrown by a person and a person from another team will try to hit it to earn some points which is called as runs. After certain point the combination will flip, so the other team will throw the ball and the team who was previously throwing the ball will try to hit it. After end of both these sessions whoever has scored the highest are considered to be a winner. 

## What is IPL?
Its a domestic cricket tournament played in India every year. Here each match consist of 20 overs for each team, one over = 6 balls, so each team can face upto 120 balls to score their runs.

## What is the objective of this model?

This model uses learns the existing data from the historical games and predicts the potential winner of the game. 

## Isn't there such models exists already?
There are plenty of machine learning models which exists online which does predict the game result based on the historical data, but what I am attempting to do is instead of predicting the entire games result, my model predictics the result for each ball being bowled and by simulating many of such games it will find the winner. 

## How does the model work?

A winner of a cricket game is impacted by various factors, starting with the set of players, venue, order at which the players bowl(throw) the ball. In this format of cricket there are some rules for such bowling order. A bowler, a person who throws/bowls the ball, cannot bowl two consecutive overs. One individual bowler cannot bowl more than 4 overs in a game. 
With this rules considering there are 11 players in the game, out of which usually 3-4 players are not good in bowling or never bowled in IPL before. With remaining 7-8 potential bowlers 20 overs has to be bowled, with the team captain's strategy the bowling combination changes based on the situation in the game. So a simple algorithm tries to list out all the possible bowling combination which can be made with the set of bowlers. But using this bowling combination can impact the model negatively since this model contains all possible combation we only need the once which are likely to happen. So using the historical bowling history of a player, a subset of the bowling combation is filtered where the probability of such bowling combation will be applied in the game is high. With this bowling combination a Gradient Boosting Classifier model is created with historical bowler vs batsman balls faced. Also venue is considered since the pitch or the venue plays a huge role in scoring. With all the thousands of bowling combination the games are simulated and the scores are averaged to see the potential winner. 

### To make it fun I am going to predict every single game of the IPL 2023 and publish it before the game starts, also I will be placing a small bet in a betting site to see how much I earn/lose by end of the tournament. Also my friend will be placing a similar bet on a team but not based on my model but based on the self intution. I thought this will be a fun experiment to conduct who makes highest number of correct prediction, a human or a ML model. 

# Follow me on my social media to get quick updates on the model prediction and the results
## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://vishnu-the-analyst.github.io/portfolio/index.html)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vishnu-eswaran/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/vishnu_k_k)
[![instagram](https://img.shields.io/badge/instagram-405DE6?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/vishnukumar_kandasamy/)

