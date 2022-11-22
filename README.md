# forecasting_retail_sales_PA

# Forecasting Ratail Sales in La Mancha

## Introduction

Our cousind from La Mancha has a grocery store and after see in the inetrnet the possiblities of Machine Learning has asked us if we can apply it into his bussines and see if we can predict the sales of one of his products.

For this task we have received the sales of every category product (_Referencia_) each date (_Fecha_) and how much made was earned (_Ventas_)

## Preprocessing and model training stages:

The procedure was clear, first we chose a product (iberian ham, as well spaniards) and after detect a weekly stationality in the model we applied some feature engineer to the dataset:




* One-hot-enconding to create a boolean parameter for each day of the week, so the model knows which day of the week is.

* shifting the sales of the product one week to give the model information about the last sales, it also allows the model to match certain values of sales with certain days since we have the boolean for the days, as we have.

After this preprocessing of the data we applied two different models:

* Random Forest: Since its simplicity and well performence this was our first choice. In order to increase its speed we decided to put the hyperparameter of the stimators to 80 instead of 100 since we observe practicly the same performance in the half of the time.

![random_forest_prediction](https://user-images.githubusercontent.com/34031559/203386313-a487e2a5-7a1d-41a5-9f86-e4a755d6432b.png)

* Support Vector Machine: In \order to check if we could have a similar performance with a even faster model we applied the support vector regressor. After play with the hyperparameters we put regulation parameter _C_ at 0.75 and we observe a very nice performance in even lower time than the Random Forest model.

![SVM_prediction](https://user-images.githubusercontent.com/34031559/203386213-a026660e-7453-4d57-a48a-f20e97c2fe73.png)






