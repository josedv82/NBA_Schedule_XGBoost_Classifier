# Influence of schedule related metrics on games outcomes in the NBA. A predictive model approach.

A google colab notebook showcasing the workflow of a model to predict NBA game outcomes and winning probabilities based on schedule related data. 

#### Data Source:
* I used an R package that I built called [{airball}](https://github.com/josedv82/airball) to [download the data](https://github.com/josedv82/NBA_Predictive_Model/blob/main/Airball_Download.Rmd). {airball} provides various functions to extract schedule related metrics from public box score information.
* To train the model I used 20 seasons of NBA data (2000-19).
* I also ran the model on 2021 season data to check its performance given some of the differences in schedule related to COVID.

#### Metrics:
* ```Game Outcome``` (model target)
* ```Distance Travelled``` Distance travelled over "X" time windows for both teams in a game.
* ```Time Zone Shifts``` Number of time zone shifs over "X" time windows for both teams in a game.
* ```Games Played``` Games played over "X" time windows for both teams.
* ```Rest Days``` Number of rest days prior to a game for both teams.
* ```Location``` Home or Away.
* ```Streak``` Consecutive Ws or Ls for both teams.
* ```Win %``` Winning % for each team.

#### The model:
* This is an example of supervised learning where a [XGBoost](https://www.kaggle.com/prashant111/xgboost-k-fold-cv-feature-importance) model was implemented. I used the [{h2o}](https://www.h2o.ai/products/h2o/) package in R to build, train and evaluate the model. 

#### Model Explainability:
* I used [SHAP](https://www.kaggle.com/dansbecker/shap-values) values to identify feature importance, as well as to explain how different features contribute to model predictions and outcome probabilities for each observation.

#### Access
The notebook has comments with more explanations about each part of the process. For access:

* A static copy of the notebook is available [here](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 
* For access to the interactive colab notebook visit [this link](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 

