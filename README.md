# 2021 T20 World Cup Predictor

## Introduction

Cricket is a tremendously popular sport all across the world, and the sport has seen a boom in viewership following the invention of the Twenty-20 (T20) format in 2002. This format promised a to deliver fast-paced, exciting cricket accessible to thousands of fans in order to draw a younger audience and since 2002 it has proven successful with a multitude of leagues played across the world introducing new people to the sport.

The highest standard of T20 games are T20 Internationals (T20I), which sees two international members of the International Cricket Council (ICC) take each other on for 20 overs each. In 2007 the ICC introduced a biannual world cup tournament in order to find the best international team. 

The 2021 ICC Men’s T20 World Cup will be the seventh edition of this tournament and takes place from 17th October to 14th November 2021. The contest is played between 12 teams (Super 12), eight of which have directly qualified and four teams from qualifying from the first round. The Super 12 are then split into two groups, and from each group 2 teams will qualify for the semi-finals. Two semi-finals will be held, and from which the winners will move onto the final. The winner of the final will be crowned champions of T20I cricket for the next two years. 

The aim of this project is to see if the winner of this tournament can be predicted. The dataset will be obtained from ESPNCricinfo, and will contains player statistics and historical result data. Six different predictive models will be used to identify the best option for future use cases, such as the 2022 T20 World Cup or Indian Premier League (IPL) 2022.  

## Methodology

The data will be retrieved from ESPNCricinfo to create a training dataset which will be used by the model. The training dataset will be formed from 1) All T20Is played by the participating teams prior to October 2021, 2) List of all players in these match 3) T20I career statistics for all players involved in the T20Is. An additional dataset with the fixtures will be used for the predictions. 

Some minor data pre-processing is required to combine all three datasets to generate the training and testing datasets. Each recorded match contains the following set of data: Team 1, Team 2, Winner, and Team 1 Features, Team 2 Features. 

| No  | Feature       | Category | Feature Description
| --- | --------      | ------- | -------                                 | 
| 1   | Matches_avg   | Team    | Mean of matches played by the team      |
| 2   | Bat_Inns_avg  | Team    | Mean of batting innings by the team     |
| 3   | NO_avg        | Team    | Mean of not outs by the team            |
| 4   | Bat_Runs_avg	| Team    | Mean of runs scored by the team  |
| 5   | HS_avg        | Team    | Mean of high score by the team  |
| 6   | HS_max        | Player  | Maximum high score by a player on the team|
| 7   | SR_bat_avg	  | Team    | Mean of batting strike rate by the team  |
| 8   | SR_bat_max    | Player  | Maximum batting strike rate by a player on the team  |
| 9   | 100s_avg      | Team    | Mean of 100s scored by the team |
| 10  | 100s_max	    | Player  | Maximum 100s scored by a player on the team  |
| 11  | 50s_avg       | Team    | Mean of 50s scored by the team |
| 12  | 50s_max       | Player  | Maximum 50s scored by a player on the team  |
| 13  | 4s_avg	      | Team    | Mean of 4s scored by the team |
| 14  | 4s_max        | Player  | Maximum 4s scored by a player on the team |
| 15  | 6s_avg        | Team    | Mean of 6s scored by the team  |
| 16  | 6s_max	      | Player  | Maximum 6s scored by a player on the team  |
| 17  | Bowl_Inns_avg | Team    | Mean of bowling innings by the team  |
| 18  | Wkts_avg      | Team    | Mean of wickets taken by the team |
| 19  | Wkts_max	    | Player  | Maximum of wickets taken by a player on the team  |
| 20  | Bowl_ave_avg  | Team    | Mean of bowling average by the team |
| 21  | Bowl_ave_min  | Player  | Minimum bowling average by a player on the team  |
| 22  | Bowl_Econ_avg | Team    | Mean of bowling economy by the team |
| 23  | Bowl_Econ_min | Player  | Minimum bowling economy by a player on the team |
| 24  | SR_bowl_avg   | Team    | Mean of bowling strike rate by the team |
| 25  | SR_bowl_min   | Player  | Minimum bowling strike rate by a player on the team  |
| 26  | 4w_avg        | Team    | Mean of 4 wicket innings scored by the team  |
| 27  | 4w_max        | Player  | Maximum 4 wicket innings by a player on the team  |
| 28  | 5w_avg        | Team    | Mean of 5 wicket innings scored by the team |
| 29  | 5w_max        | Player  | Maximum 5 wicket innings by a player on the team |

A model was then build with two different approaches in mind. This will allow us to see the predictive analysis of three classifiers (Logistic Regression, Random Forrest, & Support-Vector Machine). The two apporcahes are: 

Seperate Team Data: Each match will average the statistics of each player from the squad for both teams and create a set of features for team 1 and team 2. 

Combined Team Data: The same as unique team data but rather than two sets of features the mean of both teams will be taken into account. 

## Conclusion

The results of the models are below, it can be seen that Random Forrest Combined Team Data is the best performing model. None of the six types were able to predicted the correct winner, and with potential further improvements the model may be able to predict the winner for the next edition of the tournament. 

| Classifier              | Combined Accuracy | Combined Predicted Winner | Separate Accuracy| Separate Predicted Winner|
| ----------------------- | --------  | ------- |------- |------- |
| Logistic Regression     | 70.45%	 | New Zealand |52.27%  |West Indies  |
| Random Forrest          | 72.73%   | England |65.91%  | India |
| Support-Vector Machine  | 65.91%   | England  |54.55%  |England  |


