# Influence of schedule & travel metrics on game outcomes in the NBA. 

A notebook showcasing the workflow of a model to predict NBA game outcomes and winning probabilities based on schedule related data. 

#### Goal:
The model outcomes game predictions (along with the probability associated to winning and losing). However, my main goal was to understand how different games may be affected by schedule related metrics such as mileage, rest, density, time zone shifts, etc. This information could potentially be used by teams to optimize travel plans and manage different schedule indicators during the season.

#### Data Source:
* I built an R package ([{airball}](https://github.com/josedv82/airball)) to [scrape the data](https://github.com/josedv82/NBA_Predictive_Model/blob/main/Airball_Download.Rmd). {airball} provides various functions to extract schedule related metrics from public box score information.
* Data preparation. My code to clean the data and prepare it modeling is available [here.](https://github.com/josedv82/NBA_Schedule_Classifier/blob/main/Airball_Download.Rmd)

Once the data is ready:
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

#### XGBoost model:
* This is an example of supervised learning where a [XGBoost](https://www.kaggle.com/prashant111/xgboost-k-fold-cv-feature-importance) classifier was implemented. I used the [{h2o}](https://www.h2o.ai/products/h2o/) package in R to build, train and evaluate the model. 
* Current model performance:  
```
MSE:  0.1803835
RMSE:  0.4247158
LogLoss:  0.5333432
Mean Per-Class Error:  0.2758835
AUC:  0.8041708
AUCPR:  0.8072966
Gini:  0.6083416
R^2:  0.2784605

Confusion Matrix (vertical: actual; across: predicted) for F1-optimal threshold:
          0    1    Error        Rate
0      2495 1335 0.348564  =1335/3830
1       774 3035 0.203203   =774/3809
Totals 3269 4370 0.276083  =2109/7639

```

#### Model Explainability:
* I used [SHAP](https://www.kaggle.com/dansbecker/shap-values) values to identify feature importance, as well as to explain how different features contribute to model predictions and outcome probabilities for each observation.
* Below is an example image of how the model makes a decision for one game:

<img src="https://github.com/josedv82/NBA_Schedule_Classifier/blob/main/SHAP_Force_Plot.PNG" align="center" />

For more info on the science behind SHAP values visit this [video.](https://www.youtube.com/watch?v=-taOhqkiuIo)

#### Check Out the Code:
* A static copy of the notebook is available [here](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 
* For access to the interactive notebook visit [this link](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) to open google colab.

#### Future Work:
* Continue improving model performance.
* Identify other potential relevant features.
* Deploy model into shiny app to provide user friendly access to predictions. 

#### Other NBA related work
* [NBA Game Density APP](https://josedv.shinyapps.io/NBASchedule/)
* [airball R package](https://github.com/josedv82/airball)
