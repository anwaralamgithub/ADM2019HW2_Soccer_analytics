#### Homework_2
The Homework submission consist of a jupyter file consisting RQ1 to RQ6 and CRQ1 and CRQ2.
Details comments are available in the Jupyter notebook, where as the final discussion of Research Quaestion is defined below.

## RQ1
Who wants to be a Champion? During a season could happen that a team has bad periods. For example, more than three consecutive games lost, or it could have a positive trend where it seems to be unbeatable. Let's visualize this trends!
### Solution and Steps



## RQ2
Is there a home-field advantage? It is generally believed that there is an underlying home field advantage in sport, i.e. an highest probability of winning of the home team. Let's check for this, and see whether the outcome of the game (win, draw, lose) is correlated to the playing side (home or away). For 5 different teams of Premier League, show the contingency table (outcome x side). Therefore, perform an "overall" Chi-squared test in the following way: build a unique contingency table, that contains all the matches in which only one of the 5 teams previously selected is involved, to see whether there is home field advantage. State clearly the tested hypothesis and whether it is accepted or rejected

### Solution and steps
After importing the data, we made a scoring mechanism of win loss and draw, and then summarize the dataset in terms of wee, team, home or away over loss and winn or draw.
we have then selected 5 teams: Arsenal, Chelsea, Liverpool, Manchester City, Manchester United for our observation.
statement:
null hypothesis : if a team is playing in Home or away it will not effect their performance ; Alternative Hypo: if team is playing in their home it effects performance; we considered ALPHA as 5%

we observed that except Arsenal other teams were rejecting the NULL Hypothesis.

## RQ3
Which teams have the youngest coaches? Rank all the teams by the age of their coach and show the 10 teams with the youngest coaches. Remember that during a season a team could have more coaches, in that case pick the younger of them. Additionally, show the distirbutions of the ages of all coaches in Premier League, using a boxplot. (Hint: There's an attribute birthDate).

###solution and Steps
Imported the TEAMS Data, filtered the data from city "ENGLAND" area as for the premiiere league only and Type "CLUB" only
