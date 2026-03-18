# lol-comeback-predictor
Utilizes data from professional League of Legends tournaments to train a model that predicts how likely a team can achieve a comeback win. Data Science project for DSC 80 @ UCSD.

# Introduction

League of Legends is one of the most popular video games in the world and features one of the largest esports scenes. The dataset, provided by Oracle's Elixir, contains extensive match data for all professional matches played in 2025. The dataset has 120636 rows and 165 columns, where rows follow a pattern of 10 players and two team summaries, and each column is a match statistic or metadata being tracked. There are a few columns particulary noteworthy and will be the focus of this project:

- **result**: This column represents the outcome of a game, with 0 being a loss and 1 being a win. Due to the nature of competitive play, there are no draws.
- **kills**: This column denotes the number of kills a player ended the game with, or in the case of the team summary rows, the combined total number of kills for the entire team.
- **firstbaron**: Baron is a boss in the game that, upon killed, grants the killer's team powerful bonuses. This column denotes whether or not a team has killed the first baron, with 0 being no and 1 being yes.
- **goldat__**: Denotes how much gold a player has from 10 - 25 minutes, increasing in intervals of 5.
- **goldddiffat__**: Similar to goldat__, but instead represents the difference in gold between players of opposing teams. Therefore, it can take negative values.

The primary question of interest for this project is **how likely is a team able to pull off a comeback victory**. For this project, the criteria for a comeback victory is that a team has to win the game after having a disadvantage in gold at 15 minutes. As the average League of Legends game is 30-45 minutes, and gold differential stops being tracked after 25 minutes, being behind in gold at 15 minutes means a team has been trailing their opponents for at least half of the game. 

