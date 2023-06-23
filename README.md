# Unpeaceful_Assemblies
Predicting Violence at Demonstrations in the US
I aimed to train a Machine Learning model to predict the likelihood of violence occurring at demonstrations in the United States

## Table of Contents

- [Data](#data)
- [Methodology](#methodology)
- [Results](#results)
- [Acknowledgements](#acknowledgements)

## Data

Describe the dataset(s) used in your project. Include information on the source of the data, and any preprocessing steps you took.

I used the ACLED dataset in my project to evaluate, model, and predict peaceful versus unpeaceful demonstrations. Unpeaceful demonstrations were comprised of "Violent Demonstrations", "Protests with intervention" and "Excessive force against protesters."

I also used the Southern Poverty Law Center Hate Watch List to create a list of hate groups to check against my dataset

## Methodology
1) Define target based on SUB_EVENT_TYPE and create a binary of violent versus nonviolent demonstrations.
2) Explore tags and notes on characterization of what occurred and who was involved in peaceful and unpeaceful demonstrations
3) Take findings to create new features via keyword/tag search in various columns pertaining to information about certain groups, motivations, and miscellaneous qualities of U.S. demonstrations
4) Convert qualitative information about crowd sizes into numerical continuous values, and removing the data points that had no crowd size information.
5) Convert DATE object to datetime and create new columns for month date and year
6) Fit models and hyperparameter tune to predict target feature (used LogisticRegression, RandomForests, KNearestNeighbor, and XGBoost.

## Results

Logistic Regression had the best predictive ability for what I was scoring (recall). Model was decent at catching good proportion of True Positives (violent demonstrations) to False Negatives. Trade-off with less decent performance on characterizing True Negatives, but for the stakeholder (Public Safety Officers), would be valuable. 

## Acknowledgements 

The Armed Conflict Location & Event Data Project (ACLED)
https://acleddata.com
The Southern Poverty Law Center 
https://www.splcenter.org/