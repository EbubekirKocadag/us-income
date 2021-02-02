# us-income

## What

After some work on model evaluation, we start a little project about how to evaluate our model. In this project, we tried to have the best score without beeing overfit. We have, as dataset, people in The US with there social status and the target value is their income.

## Why

We do this project to have a better understanding of models and their evaluations.

## When

We do this project during our BeCode training from 1st February 2021 to 2nd February 2021.

## How

We create all the project on jupyter notebook to have a better readability. To be able to run this project you have to install pandas, numpy, SKlearn and matplotlib. All data and preprocessing are in the data repository, so you can check and have a better understanding of how all the data is done.

Once we had everything installed, we start by searching the baseline accuracy by just using the RandomForestClassifer without giving a specific parameters. After the fit we search the accuracies and the f1 score. For X_train score we had 99.99%, X_test 85.45% and f1 66.45% so we can easily see just by looknig the difference between X_train and X_test that we have an overfit. After that, to have a better score, we search the best parameter for our model with GridSearchCV by giving it a set of parameter. We choose n_estimators, max_depth, max_features and oob_score as parameters to be changed. This decision was taken on the basis of the influence of how the random forest is made. We had around 288 fits to our model and grid search determine the best one which is n_estmators = 400, max_depth = 12, max_features = None and oob_score = True. !!!!!!!!ici faut voir l'histoire du overfit et tout !!!!!!!!

We start to evaluate our model with Roc curve to see if we have an overfit or not and to see if we have to change the threshold from 0.5 to an other value. Here, we something that we did not really understand because when we serach for f1 score with 0.4 as threshold we had a greater f1 score than calculating the best threshold.

We didn't want to stop here and we continue to search a way to have a better score so we decide to do a resampling but we couldn't found a score worth the trouble (only 3% more for the f1 score). We conclued that we probably didn't choose the best parameters to test with our gridSearchCV or maybe the preprocessing was not made correctly. As we hadn't much time we decided to stop here and start to plot.

## Who

[Melvin Leroy](https://github.com/Melvin-Leroy), junior AI developer

[Ebubekir Kocadag](https://github.com/EbubekirKocadag), junior AI developer

## Pending things to do

As we already sad on "How", you can try to redo the preprocessing or improve it, you can try other parameters on GridSearchCV (but be carful with these value it takes more than 30 min).
