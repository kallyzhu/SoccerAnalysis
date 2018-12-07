# SoccerAnalysis

## Objective
<li>Investigate factors that might affect a soccer team’s performance<\li>
Build a Random Forest Regression Model to predict the goal difference for a match
Simulate 2018 World Cup matches and generate a distribution of possible champions

## Data processing
Our initial dataset contains more than 30,000 international matches from 1950 to 2017. Also, with domain knowledge in soccer, we cleaned and processed data as the followings:
We added two new variables,(team1Home, team2Home)to indicate whether or not the teams were playing at home.
We exclude the friendly matches and outliers, like some teams would score more than 10 goals in a single match for our analysis.
We made a reverse for each entry to reflect the result for every team.
We merged various datasets in order to map confederation strength coefficient for each team. 
To simulate the World Cup, we merged the world cup group match schedule with the feature data frame which contains all the training variables for each team. 

## Statistical analysis
We plotted the average total score per year from 1956 to 2017 using groupby function and seaborn/matplotlib package.
We plotted the winning percentage for each team with friendly matches and without friendly matches.
We compared the winning percentage for each team whether it was playing at home or not.
 
## Model building
 We extracted three main features to predict the score for each team.
Feature1, if a team played at home.
Feature2, the league strength for both team1 and team2; we merged teams dataframe into matches.
Feature3, the winning, drawing, losing rate and the average goal difference of the recent 5, 10, 20 and 40 matches for each team.
We trained our model using random forest regressor with GridSearchCV to make predictions about the goal difference and evaluated its performance by the RMSE measure.
We also built a random forest classifier to predict categorical variable, which converted goal difference to win-draw-lose. The accuracy rate thus has increased from 0.260 to 0.539.




## Simulate 2018 Russia World Cup
We reconstructed a dataframe with 32 world cup teams, simulated each game and predicted win-draw-lose result. We randomly alternated the sequence of team1 and team2 to produce more outcomes. 
Each simulation consists of a group stage and several knockout stages. Teams only play against each other within their own groups. The group winners and the runner-ups would move on to the knockout stages (round of 16, quarter finals, semi finals and final). The simulation strictly follows the FIFA World Cup rules and reflects as much reality as possible. 
We simulated the World Cups 10,000 times and got a distribution of possible champions over the 32 world cup teams.



## What to improve in the future 
We could redesign our feature variables or even incorporating new features such as data about actual players, e.g. player’s market value, age, height, weight etc. That would require a significant amount of work in data preprocessing. Also, ML-wise, we need to try out new models to improve our prediction. 

## Why you should invest in our group
The simulation indicated Brazil would most likely win the Russia World Cup, which is consistent with the predictions of Microsoft's AI and data science expert Sorin Peste. Even though in reality Brazil flunked in the semi-final when playing against Belgium, France holds the second place in our prediction. So, if you betted for France, you would still win a decent amount of fortune. Therefore, by investing in our analysis and making progress in our machine learning models, we would make better predictions and help you win more money for the next world cup. 

