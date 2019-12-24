#deep_learning_pe

* Authors: Michael Pelton, Susan Chen, Nikhil Kamoji, Ziyu Zhang

*The objective of this project is to identify at any point in time, the relative investment potential and attractiveness of certain sectors (for example: healthcare, energy etc.) for a private equity fund given the current market and economic environment. The end goal is to build a deep learning model that will rank major market sectors for growth potential and investment attractiveness that may eventually be used by a PE fund to guide sector targeting at a particular point in time.
As an example, a question that the results of the model might answer could be something along these lines: “Is energy a good bet right now given the fund horizon / market predictions etc.?”*

*Contents / Files*

*Notebooks: To be run in the following order*

1) combined_indicators.ipynb – read in and process macroeconomic indicator data. Data comes in at differing intervals from daily to quarterly so unique dates must be identified, data must be read in and then concationated as to populate one dataframe for output into the next step. Output dataframe is indexed by date and each column represents an indicator. Output of this notebook is ‘combined_indicators.csv’

2) combined_sector.ipynb – read in and process sector data for all 9 sectors in scope for our model to rank. Output is a dataframe where rows are dates and columns represent each sector. Output of this notebook is ‘raw-data.csv’

3) daily_data_minipulate.ipynb – combined_indicators.csv and raw-data.csv are taken as inputs here. Dataframes are joined and data is forward filled in order to account for some indicator data coming in monthly and quarterly. Output of this notebook is daily_final.csv 

4) Data_model_shift.ipynb: shifts daily_final.csv data in a way as to allow for model to predict movement 125 days into the future and eventually let us recommend sectors for investment. This time frame of 125 days can be changed by the degree of shift. Output of this notebook will be shifted data for the models to be trained on for each individual sector. Data saved in the data folder. 

5) project-DNN.ipynb: Deep Feed-forward neural network which produces ranked output

6) project_lstm.ipynb: LSTM model which produces ranked output 

*Data Files and Folders*

1) data: folder containing market return data for all sector etf daily returns and the S&P 500 as a whole 

2) indicator_data: folder containing all macroeconomic indicator data used in the model

**All other csv data files are created from the 2 above folders by running jupyter notebooks outlined above.**




