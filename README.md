# Capstone-Project-_Stock-Price-prediction-Kaggle-Data-Qualcomm

Stock Closing Price Prediction using Deep Learning, TensorFlow2 &amp; Keras

**INTRODUCTION**

Forecasting the stock exchange data is an important financial subject which involves an assumption that the fundamental information publicly available in the past has some predictive relationships to the future stock returns. Stock market forecasting contains uncovering the market trends, planning investment tactics, identifying the best time to purchase the stocks and which stocks to purchase. Stock price prediction is a heated topic in prediction study of the financial area. The stock market is essentially a non-linear, nonparametric system that is extremely hard to model with any reasonable accuracy.

**Objective**

The objective of this model is to give an approximate idea of where the stock price may be headed.There are way too many reasons to acknowledge for the long term output of any stock. Many things and parameters may affect the prediction and training model here only on the basis of price trend is tested.This model based on GRU to predict the closing price of a stock.Due to smaeller size of the dataset available on Kaggle GRU model is Preffered.

**Approach to solving the problem**

We will try to predict stock market closing prices for qualcomm Stock in NYSE using GRU, a state-of-art deep learning algorithm for sequential data.Two main purposes of the analysis of time-series are: 

(a) identify the nature of the observation sequence phenomenon and

(b) foresee (accurately predict time-series variable).

These two objectives require the identification of the patterns of time series observed as well as a formal description. We can interpret and embed the pattern with other records once the pattern has been identified.

We shall be using following Steps/Aproach to generate the databuild

Data cleaning-->Data modeling-->Visualisation of Data-->Feature Scaling-->Build a predictive model-->Evaluate the model



**Model summary**

The model we used is a stacked GRU. So the output of one GRU layer acted as the input to the next GRU layer stacked above the former one and so on. The GRU/LSTM layers in Keras expect the input to be in three-dimensional. Thus, we have to make sure that the output from a previous layer is formatted in a three-dimensional way so as to provide it as input to the next layer. This job could be achieved by setting return_sequences=True in the GRU layers whose output would potentially act as the input to the next GRU layer.

model architecture.

Total params: 220,301
Trainable params: 220,301
Non-trainable params: 0

model score
Train Score:
MSE: 0.00026 , RMSE: 0.02
Validation Score:
MSE: 0.00142 , RMSE: 0.04
Test Score:
MSE: 0.02870 , RMSE: 0.17

**Inference**

GRU uses less memory and is faster than LSTM, however, LSTM is more accurate when using datasets with longer sequences.
A neuron is designed to be activated based on the information it is getting from the previous layer. And with each layer, the complexity of the data captured by the network increases. Thus, we can consider the number of neurons and the number of layers to be hyper-parameters and we tune them(increasing/decresing the number of neurons/layers) based on the results we observe. We would tend to increase the number of layers/neurons if we observe that the model is underfitting the validation data. Similarly, we would tend to decrease the number of layers/neurons if we observe that the model is overfitting the validation data. So basically, we train on the train data, tune the hyper-parameters based on the performance on the validation data, and finally check the model performance on the test data.

**References**

cloudxlab repositery
Kaggle 
