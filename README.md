# 2021 T20 World Cup Predictior

## Introduction

Cricket is a tremendously popular sport all across the world, and the sport has seen a boom in viewership following the invention of the Twenty-20 (T20) format in 2002. This format promised a to deliver fast-paced, exciting cricket accessible to thousands of fans in order to draw a younger audience and since 2002 it has proven successful with a multitude of leagues played across the world introducing new people to the sport.

The highest standard of T20 games are T20 Internationals (T20I), which sees two international members of the International Cricket Council (ICC) take each other on for 20 overs each. In 2007 the ICC introduced a biannual world cup tournament in order to find the best international team. 

The 2021 ICC Men’s T20 World Cup will be the seventh edition of this tournament and takes place from 17th October to 14th November 2021. The contest is played between 12 teams (Super 12), eight of which have directly qualified and four teams from qualifying from the first round. The Super 12 are then split into two groups, and from each group 2 teams will qualify for the semi-finals. Two semi-finals will be held, and from which the winners will move onto the final. The winner of the final will be crowned champions of T20I cricket for the next two years. 

The aim of this report is to see if the winner of this tournament can be predicted. The dataset will be obtained from ESPNCricinfo, and will contains player statistics and historical result data. Six different predictive models will be used to identify the best option for future use cases, such as the 2022 T20 World Cup or Indian Premier League (IPL) 2022.  

## Theory

## Conclusion

| Classifier              | Combined | Separate |
| ----------------------- | -------- | ------- |
| Logistic Regression     | 70.45%	 | 52.27%  |
| Random Forrest          | 72.73%   | 65.91%  |
| Support-Vector Machine  | 65.91%   | 54.55%  |

## How To Use

#### The T20 Record Obtainer

This notebook is used to obtain all required data to be fed into the model. The data will be parsed from https://www.espncricinfo.com/, which is a cricket sports website, and a database. 

The outputs of this script are:

1. match_url.csv (All T20I matches played prior to the World Cup including stats from the matches)
2. match_data.csv (All players that were involved in matches recorded in 1.)
3. player_data.csv (Statistics of all players that were involved in all recorded matches)
4. player_match_data.csv (Same as 2. but includes each players country required for data preprocessing)
5. player_squad_data.csv (Based on the selected squads for the tournament all statistics for selected players) 

Note: It is not recommended to run this script as the parsing takes significant time.

#### Data Preprocessing 

#### Combined Stats Model

#### Seperate Stats Model

