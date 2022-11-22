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

* Random Forest: Since its simplicity and well performence this was our first choice. In order to increase its speed we decided to put the hyperparameter of the stimators to 80 instead of 100 since we observe practicly the same performance in the half of the time. The results we obtained in _32.8s_

![random_forest_prediction](https://user-images.githubusercontent.com/34031559/203390999-038e07c3-0901-46bd-9a63-c432297c2c50.png)


* Support Vector Machine: In \order to check if we could have a similar performance with a even faster model we applied the support vector regressor. After play with the hyperparameters we put regulation parameter _C_ at 0.75 and we observe a very nice performance in even lower time than the Random Forest model. In this case we obtained our results in _3.5s_

![SVM_prediction](https://user-images.githubusercontent.com/34031559/203391237-47481c69-aec2-4655-ab56-a386ed4088c3.png)
