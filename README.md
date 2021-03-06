# ReadMe: Dashboard - LSTM Neural Networks and HAR Models for Realized Volatility - An Application to Financial Volatility Forecasting

This repository aims to illustrate the results of the thesis - LSTM Neural Networks and HAR Models for Realized Volatility - An Application to Financial Volatility Forecasting. This repository only contains code for the dashboard, all the remaining code is located [here](https://github.com/nickzumbuehl/master_thesis).

## General Infomation
The dashboard runs under the url: http://nick-vola.herokuapp.com. Please note that the website might take a moment to load, as free herokuapps go to sleep mode when not used for 30 minutes. Moreover, free heroku apps are limited to run up to 1000 hours per month. In the unlikely case that the web application fails to load, please contact the author of the paper.

Alternatively, the dashboard can also be run locally. To run the dashboard on your local machine please follow the subsequent steps:
1. make sure you have all necessary dependencies installed on your local machine. All dependencies are listed in [```requirements.txt```](requirements.txt).
2. run [```dashb.py```](dashb.py) in the terminal by typing: ```python dashb.py```
3. copy paste the url from the terminal to your local browser to open the dashboard.

## Dashboard Structure
The dashboard takes the data input produced by [```dashboard_data_prep.py```](https://github.com/nickzumbuehl/master_thesis/blob/master/masterthesis/dashboard_data_prep.py). This data are then visualized and accuracy measures are computed.

### Visualization
#### Time Series Plot
This plot shows the time series of the predicted realized volatility measures for the models selected in the dropdown menu. Moreover, one can choose for which data set and period the time series should be plotted. Please note, the actual series is called ```future``` in the dropdown menue.

#### Bias Plots
The bias plot show the distribution of the biases. The y-axis is computed as ```predicted realized volatility - actual realized volatility```. A large positive value thus implies an over-prediction, whereas a small value indicates an under-prediction.

#### Mincer Zarnowitz Scatter Plot
This scatter plots shows the actual values versus the predicted values. More specifically, the x-axis depicts the predicted values, whereas the y-axis depicts the actual realized volatility measures. Naturally, the closer the points in the scatter plot are to the 45 degree line, the better the prediction. 

### Accuracy Measures
The table reports the most important accuracy measure, including the ```MAE```, ```MAPE```, ```MSE```, ```Mincer-Zarnowitz R-Squared``` and ```Mincer-Zarnowitz Beta```. The accuracy measures are discussed more thoroughly in the text version of the thesis.






