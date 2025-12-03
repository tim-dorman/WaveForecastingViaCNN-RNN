# WaveForecastingViaCNN-RNN
This project used Deep Learning modeling via CNNs and RNNs to create a 24 hour look ahead surf forecast based on NOOA NBDC Buoys


ave forecasting for the sport of surfing is an exercise thats been going on since the sport's creation. It is a common occurence for surfers to try and predict wave surfability in the future from present and histroical conditions. In fact, there are companies dedicated to the purpose of forecasting waves for surfers that rely on user subscriptions to gain revenue.

Additionally, there is a wealth of free data available, on present and historical surf conditions, provided by NOAA via the National Data Buoy Center. So, the question that arises is: Is there a way to apply deep learning methodology to this freely available data, to create a reliable wave forecasting tool?

Neural Networks, such as CNN and RNN are often used in image classification and text classification use cases, but there are additional novel uses for CNN and RNN with time-series data. This use of sequencing allows one to utilize CNN and RNN models to analysze this data. This project uses LSTMs (vanilla LSTMs and Bidirectional LSTMs) as well as 1D CNN models for frorecasting time series data (by way of regression and classification).

This project will attempt to apply RNN and CNN models to time series data collected by NOAA Buoys and use this data to forecast surf conditions 24 hours ahead of the present moment in time. The surf conditions that will be predicted are:

A) Surf Score: feature engineered metric created to represent physical surf conditions (wave height, period, and wind speed) converted into a 0-10 scale.

and

B) Surf Label, a.k.a. "surfability": A binary classification of whether not the present surf conditions are surfable or not (also feature engineered from domain knowledge of physical surf conditions)

These target metrics will be predicted by six separate models. The surf score will be predicted via regression modeling, and the surfability will be predicted via binary classification modeling.

In fact, a related work has been done using LSTMs to predict ocean wave conditions. Minuzzi and Farina (2023) used time series buoy data on a select number of buoys off of the Brazilian coast to try and predict a significant wave height change via LSTMs

Unlike the study mentioned though, this project will attempt to understand overall wave conditions as it relates to surfing given time series buoy data via the feature engineered metrics of surf score and surf label (surfability). Additionally, this project will use all of the buoys within the NOAA NBDC network, and will apply CNNs and BiLSTMs to this data rather than simply LSTMs.


The six separate models that will be created in this project are:

1A. Vanilla LSTM Regression Model

1B. Vanilla LSTM Classification Model

2A. 1D CNN Regression Model

2B. 1D CNN Classificatioon Model

3A. Bidirectional LSTM Regression Model with Hyperparameter tuning

3B. Bidirectional LSTM Classification Model with Hyperparameter tuning

A Note on runtime: If you are planning on running this notebook to replicate the results, it is suggested to use a T4 GPU (or similar GPU spec) with HIGH-RAM. Using lower ram specs will result in kernel crashing.

Data Citation (also in Citation section at bottom of notebook):

National Data Buoy Center. (1971–2025). Standard Meteorological (stdmet) historical buoy data. NOAA.https://www.ndbc.noaa.gov/data/historical/stdmet/
