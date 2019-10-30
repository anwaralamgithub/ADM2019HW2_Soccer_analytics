#### Homework_2
The Homework submission consist of 
#### main.ipynb a jupyter file consisting RQ1 to RQ6 and CRQ1 and CRQ2.
#### theory.ipynb a jupyter file consisting of theoretical part

Details comments are available in the Jupyter notebook, where as the final discussion of Research Quaestion is defined below.

## RQ1
Who wants to be a Champion? During a season could happen that a team has bad periods. For example, more than three consecutive games lost, or it could have a positive trend where it seems to be unbeatable. Let's visualize this trends!


### Solution and Steps

After importing the data, we made a scoring mechanism of win loss and draw, and then summarize the dataset in terms of week, team, home or away over loss and win or draw, we have plotted the result with a colour picking function to plot the teams different, and to identify the the loosing and winning streak , the observation from the graph is below.

The Manchester City has the longest winning streak from week 2 till week 20, followed by the runner-up team in longest winning streak is Tottenham Hotspur from week 25 to week 32.

The team West Bromwich Albion has the longest lossing streak from week 24 till 32, followed by second longest lossing streak by Crystal Palace with effect from week 1 till week 7.



## RQ2
Is there a home-field advantage? It is generally believed that there is an underlying home field advantage in sport, i.e. an highest probability of winning of the home team. Let's check for this, and see whether the outcome of the game (win, draw, lose) is correlated to the playing side (home or away). For 5 different teams of Premier League, show the contingency table (outcome x side). Therefore, perform an "overall" Chi-squared test in the following way: build a unique contingency table, that contains all the matches in which only one of the 5 teams previously selected is involved, to see whether there is home field advantage. State clearly the tested hypothesis and whether it is accepted or rejected

### Solution and steps
After importing the data, we made a scoring mechanism of win loss and draw, and then summarize the dataset in terms of week, team, home or away over loss and win or draw.

we have then selected 5 teams: Arsenal, Chelsea, Liverpool, Manchester City, Manchester United for our observation.
statement:


null hypothesis : if a team is playing in Home or away it will not effect their performance ; Alternative Hypo: if team is playing in their home it effects performance; we considered ALPHA as 5%

we observed that except Arsenal other teams were rejecting the NULL Hypothesis.

## RQ3
Which teams have the youngest coaches? Rank all the teams by the age of their coach and show the 10 teams with the youngest coaches. Remember that during a season a team could have more coaches, in that case pick the younger of them. Additionally, show the distirbutions of the ages of all coaches in Premier League, using a boxplot. (Hint: There's an attribute birthDate).

### solution and Steps
Imported the TEAMS Data, filtered the data from city "ENGLAND" area as for the premiiere league only and Type "CLUB" only.
then we imported the Coaches data, and from the current date we mapped their ages.
we then associated the coaches with team from WYID and then ranking the team with youngest coach

secondaly we constructed the BOX PLOT and observed :


The coloured line in the box is the average of ages, upper and lower edges of the box reflects Q3 and Q1. The two Circles on the top are the outliers ageing more that 60 years. We observed that ages are centered around 47 to 52 Years

## RQ4
 Find the top 10 players with the highest ratio between completed passes and attempted passes. For this task, consider all the different types of passes, and as specified in the website, a completed pass has tag 1801 (accurate event).

In order to avoid meaningless results (e.g. players who played few minutes, and completed 2 passes over 2, achieving 100% ratio), select an arbitrary threshold of minimum attempted passes, in order to consider only the subset of players that played enough. Justify the choices you make.

### Solution and Steps

imported the Event file, after driving the desired column for the solution we took a filter on passes that is tag 1801, then counted and summarizing the Sucessive pass, we defined that thrush hold of 25 passes easch player in each event. if a player has less than 25 passes in each game we have ignored that data, as we considered that this player has not played enough time in the game.
then we calculated the success rate of passes and sort the list.
as we know that the goal keeper is role in a match that mostly passes to defenders and its ratio will be maximum and biased the results

so we removed the goal keepers from the player data.
and then finalize the top 10 player with maximum success rate in pass.

## RQ5

 Does being a tall player mean winning more air duels? Soccer is a physical game, and it happens often in a match that players are involved in air duels (i.e. when two players are contending for the ball while it is not on the ground). Make a plot that shows the dependency between height of the player and the ratio of air duels won with air duels attempted. The visualization should be a scatterplot, where each point (x,y) represent a player whose height is equal to x, and that has a ratio of winning air duels equal to y. Furthermore, color any point according an arbitrary selection of categories of height (e.g. yellow: 160-165cm, orange: 165-170cm, etc.)

Remember that the "Air Duel" is a subevent of the event "Duel" and that an air duel is said to be won if it has the tag "1801". Same as in RQ4, choose a threshold of minimum air duels attempted, in order filter your data, get reliable results, and justify your choice

### Solution and Steps

Similar to RQ4 we consided 101 tag for airduels , setting up thr thrush hold to 5 air duels for atleast quality in the data set for playing enough time in the game.
we importred the players data for height and co relates the success rate of air duels with height  and observed


Based on the scatter plot it can be seen that from heigth range 170 to 185 the success rate is from 20% to 60% whereas for range 185 to 195 the success rate 45% to 90% which clearly refelcts that height and success rate is directly proportoinal.

## RQ6
We will observe that which are the top 10 nationlities playing in Premier league

### Solution and Steps

we considered the nationality of player from passport area columns in the data. we considered on premiere league datae.
firstly we took the players id played in premiere league and then mapped their nationalities and made a barplot , from which we observed that nationality with England is highest in the league.

## CRQ1

What are the time slots of the match with more goals? Let's analyse and visualise the goals distribution into 9-minutes sets for all the matches. I.e., let's transform the minute of a goal from a continuous variable in a discrete variable (e.g. A goal scored in 5th minute, will end up in the interval 
Remind that every match goes usually from minute 0, to minute 90, but in football it is always added an arbitary amount of extra-time to every half of the match, thus consider also the intervals "45+" and "90+".



(i) Make a barplot with the absolute frequency of goals in all the time slots.
(ii) Find the top 10 teams that score the most in the interval "81-90".
(iii) Show if there are players that were able to score at least one goal in 8 different intervals



### Solution and Steps

after importing the dataset from Events, we calcuted the GOALS event , i.e. tag 101 and filtered only shots, removing save attempts
we then changed the timming into minute and made the desired range of minutes in slabs


Result (i) : Barplot with the absolute frequency of goals in all the time slots : observed that most goals are made in the middle of second half of the game.


Result (ii) : Find the top 10 teams that score the most in the interval "81-90" : observed that Mancester city scored maximum goals in the desired slot.



Result (iii) : Show if there are players that were able to score at least one goal in 8 different intervals : so we observed that there is no player who has made a goal in all the intervals.


## CRQ2

Visualize movements and passes on the pitch! Here we try to focus our attention on the zones that a player covers during a match. For each event, we have a pair of coordinates, that are respectively the starting and ending point of that event. It can be helpful to follow this link.

Knowing all the different positions where events happen, let us be able to create different types of visualizations:

1. Considering only the match Barcelona - Real Madrid played on the 6 May 2018:
visualize with a heatmap the zones where Cristiano Ronaldo was more active. The events to be considered are: passes, shoots, duels, free kicks.
compare his map with the one of Lionel Messi. Comment the results and point out the main differences (we are not looking for deep and technique analysis, just show us if there are some clear differences between the 2 plots)


2.Considering only the match Juventus - Napoli played on the 22 April 2018:
visualize with arrows the starting point and ending point of each pass done during the match by Jorginho and Miralem Pjanic. Is there a huge difference between the map with all the passes done and the one with only accurate passes? Comment the results and point out the main differences

### Solution and Steps

importing the desired match and evenets of pass, Duels, free kich and shots of the designated players. converting the coordinates on the field , designing the soccer pitch and mapping the heat map visualization.

Result (1) : Ronaldo is a good CAM player that well equipped with good dribbling and finishing skills. At times he even play as CF/Striker to support attack or as contingency plans

where as We can observe that messi is more of CM (center-midfielder) player and more support striker and forwards and inclined to left side.


Result (2) : Jorginho's intensive role is right wing, however he is supporting right and center strikers and forwards
where as Pjanic role is right wing, but he is more active on center one-third of the pitch in comparison to Jorginho. It should be mentioned that generally Jorjinho support other players more than Pjanic







