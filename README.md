This is the final project for CS696 Big Data. Here, we will be looking at multiple decision models in regards to predicting the stock market and comparing them based on how complex they were to set up, how robust they were, and how accurate they were. 
The purpose of assignment is to learn about Time Series and how to apply analysis tools for forecasting a time series. We have learned the concept and attribute of time series. In this project, we are focusing on analyzing the univariate series which is single dimension series. 

We will be using several libraries for this project:

Standard Libraries:
pandas: Data Analysis Tool
numpy: A tool for scientific computing
sklearn: Contains multiple models for machine learning

New Libraries:
+ yfinance: This tool allows us to collect stock market data from Yahoo for any range of dates. 
    https://pypi.org/project/yfinance/
    
    $ pip install yfinance --upgrade --no-cache-dir
    $ conda install -c ranaroussi yfinance
    
    The above are two ways to install yfinance.
    
+ talib: 
    This tool lets us obtain stock market statistics from a pandas column. e.g. We can get say the EMA (Exponential Moving Average) of each date when given a pandas column.
    https://blog.quantinsti.com/install-ta-lib-python/
    Unfortunately, we can't use pip on this library directly, so we had to first download the library then install it manually. Instructions can be found in the link above. Essenitally, you want to download the correct version of talib based both on your version of python and the number of bits in your processor. Then, go the directory where the file is located then run a command similar to this:
    
    pip install TA_Lib-0.4.17-cp37-cp37m-win_amd64.whl

    The 37 here represents the python version and the 64 represents a 64 bit processor. 

+ tensorflow: This framework support for building Machine Learning models. We will use Keras library to create and train a model in specific.

With that being said, here are brief descriptions of the machine learning models that we'll primarily be looking at.

Machine Learning Models: 

Decision Tree:

    A decision tree, as the name implies, is a tree structure used to guess something. Each node represents a choice, for example if this value is less than 10, we'll go left and vice versa. The tree can have many nodes to determine its predicition. Decision Trees can be further split into two types, classifcation and regression. A classification tree is where we attempt to use the given data to classify it as something. For example, the class flower problem, given  various characterstics of a flower, can we guess which species is it. Regression trees on the other handis meant to try to predict a value instead. In our case, can we predict the next stock price using this tree.


Support Vector Regression (SVR):

    Similar to what was stated above, Support Vector Regression is used to try to predict the values that we want from the data.Unlike other regression models, which try to minimize the error between the predicted and actual value, SVR tries to keep within a certain error threshold instead. This is useful for when there are a lot of outliers in the data as it will use as mcuh data as possible within the appropriate bounds.

Linear Regression:

    Similar to the SVR model, Linear Regression attempts to create a best fit from the given data to try to predict what we need. As the name implies, this model is best suited when the data follows a linear relationship between the dependent and independent variables and suffers when the data is non-linear.

Recurrent Neural Network (RNN):
    
    An RNN, is a neural network whrere nodes are connected to form a directed graph in the order data arrives. They can process variable lengths of input and can display dynamic behavior on account of the currrent history of the data. The big draw is that an RNN, using a feedback loop, will also use its previous outputs as well when deciding something
    
Long Short-Term Memory (LSTM):
    
    LSTMs can be considered a variant of an RNN. The main difference is that LSTM nodes have a cell dedicated to memory or history. This is useful to learning information over long periods of time and use that information for current needs.

* Here is the jupyeter notebooks we uploaded Google's cloud server. You can run it directly from Google server; however, it require a Google account to sign in.

+ [Decision Tree notebook](https://colab.research.google.com/drive/1BRA_v4agpq1Hj-LAA8I3cZ9g0nWwQn3P?usp=sharing)

+ [Support Vector Regression](https://colab.research.google.com/drive/1jcTqDtYeI7HVHUSkHXOt2YO1-VdXf0Os?usp=sharing)

+ [Simple Recurrent Neural Network notebook](https://colab.research.google.com/drive/1OfV2tlfGXFPxFzg8T14g_EUDHgWjuxIg?usp=sharing)

+ [Long Short Term Memory notebook](https://colab.research.google.com/drive/1fuo8hhU0tLIU8McQOgFMwuM0KGkhiY3Y?usp=sharing)
