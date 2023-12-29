# EU Soccer League SQL

This dataset contains 7 tables, including Country, League, Match, Player, Player_Attributes, Team, Team Attributes. By understaning each table and data cleaning, we will know what can be executed in the following data analysis with SQL.

Data comes from this Kaggle: https://www.kaggle.com/code/dimarudov/data-analysis-using-sql/input


## Exploratory Data Analysis
- Which country and league scores the most over the years?
    From the above table, we can know that Stade Rennais FC and Olympique de Marseille from Frace Ligue 1 (France) scored the most over years.
- Is the player's age and height relevant to their performance?
  ![q2-1](https://github.com/lantisseverus/EU_Soccer_League_SQL/assets/66398727/804d1ecc-4928-4dca-952a-3fe29f014032)
  ![q2-2](https://github.com/lantisseverus/EU_Soccer_League_SQL/assets/66398727/1d2efcc7-e30f-4c5d-a971-26cc64599fce)
  ![q2-3](https://github.com/lantisseverus/EU_Soccer_League_SQL/assets/66398727/958dd4d6-6991-4b65-b715-9ecf929c7582)
  ![q2-4](https://github.com/lantisseverus/EU_Soccer_League_SQL/assets/66398727/8617672f-31de-46c2-bc51-5bc71dbf978a)
- Does the Team's shooting chance create more goals for the team?
- Does the Team's defense width lead to fewer goals for their rival team?


## Result and Limitation

My last chunk of exploratory data analysis does not quite answer the question of whether the rival team's performance is affected by the home team's defense indicators. 

This is one of the limitations that I should aggregate the indicators respectively given their team, and whether they are home or away team in the match. Or, maybe I should pivot the table and add one more column to distinguish the home and away teams. 

Another limitation is that I have limited knowledge of soccer games. Even though I picked some of the numeric indicators and attempted to quantify their performance, I wasn't sure if the indicators were meaningful for goal or defense. 

The other limitation is that we got some missing values in the indicators for the particular team such as Ruch Chorzów, but we didn't know why the value is missing and can only replace the missing value with 0 for now. 

The result still suggests some interesting findings: 

1. Player Height plays a role in player performance but it does not suggest any causation; 
2. Player ratings grow with their experience; 
3. Chance of shooting has mild association with the goal
4. Defense pressure and defense team width are of mild association with the goal and one cannot know if it's truly valid to the rival team. Defense aggression is a bit higher among all the indicators but it's still moderate. Not sure if morale (which can hardly be quantified) plays a confounder in the causation.
