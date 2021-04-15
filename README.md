# Predicting NBA game outcomes using schedule data

A colab notebook showcasing a model to predict NBA game outcomes based on schedule related data. 

#### Data Source:
* The data was sourced with my package [{airball}](https://github.com/josedv82/airball)
* To train the model I used 20 seasons of NBA data (2000-19).
* I also ran the model on 2021 season data to check its performance given some of the differences in schedule related to COVID.

#### The model:
* This is a [XGBoost](https://xgboost.readthedocs.io/en/latest/) model. I used the [{h2o}](https://www.h2o.ai/products/h2o/) package in R to build, train and evaluate the model. 

#### Model Explainability:
* I used [SHAP](https://www.kaggle.com/dansbecker/shap-values) values to identify feature importance, as well as to explain how different features contribute to predictions and outcome probabilities for each observation.

### Access
* A static copy of the notebook is available [here](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 
* For access to the interactive colab notebook [here](https://github.com/josedv82/NBA_Predictive_Model/blob/main/NBA_Schedule_xgboost.ipynb) 

