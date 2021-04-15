# Predicting NBA game outcomes using schedule data

This notebook showcases a predictive model that aims to guess game outcomes using schedule related data. 

#### Data Source:
* The data was sourced with my package {airball}.
* The model was trained on 20 seasons worth of NBA games between 2000-19 seasons.
* I also ran the model on 2021 season data to check its performance given some of the differences in schedule related to COVID.

#### The model:
* This is a XGBoost model. I used the {h2o} package in R to build, train and evaluate the model. 

#### Model Explainability:
* I used SHAP values to identify feature importance, as well as to explain how different features contribute to predictions and outcome probabilities for each game.

### Access
* The an static copy of the notebook is available here. 
* And access to google colab notebook here. 

