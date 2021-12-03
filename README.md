# 2021-T20-World-Cup-Prediction-ML

**How to:**

**The T20 Record Obtainer**

This notebook is used to obtain all required data to be fed into the model. The data will be parsed from https://www.espncricinfo.com/, which is a cricket sports website, and a database. 

The outputs of this script are:

1. match_url.csv (All T20I matches played prior to the World Cup including stats from the matches)
2. match_data.csv (All players that were involved in matches recorded in 1.)
3. player_data.csv (Statistics of all players that were involved in all recorded matches)
4. player_match_data.csv (Same as 2. but includes each players country required for data preprocessing)
5. player_squad_data.csv (Based on the selected squads for the tournement all statistics for selected players) 

Note: It is not recommened to run this script as the parsing takes siginicant time.  
