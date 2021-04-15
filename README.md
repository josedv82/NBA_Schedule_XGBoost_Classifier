# Predicting NBA game outcomes using schedule data

This notebook showcases a predictive model that aims to guess game outcomes using schedule related data. 

#### Data Source:
* The data was sourced with my package [{airball}](https://github.com/josedv82/airball)
* The model was trained on 20 seasons worth of NBA games between 2000-19 seasons.
* I also ran the model on 2021 season data to check its performance given some of the differences in schedule related to COVID.

#### The model:
* This is a [XGBoost](https://xgboost.readthedocs.io/en/latest/) model. I used the [{h2o}](https://www.h2o.ai/products/h2o/) package in R to build, train and evaluate the model. 

#### Model Explainability:
* I used [SHAP](https://www.kaggle.com/dansbecker/shap-values) values to identify feature importance, as well as to explain how different features contribute to predictions and outcome probabilities for each game.

### Access
* A static copy of the notebook is available [here](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 
* And access to google colab notebook [here](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 

