# Forecasting Police Killings

## Motivation
With the rise of the Information Age, practically everyone now has a camera phone, allowing for an unprecedented view into the lives of everyone. Unfortunately for the police officers who are interested in power abuses, this has exposed their wrongdoings. In 2013, the acquittal of George Zimmerman began the Black Lives Matter (BLM) movement, and the killings of Eric Garner and Michael Brown in 2014 solidified police violence as a front-burner issue in the minds of BLM supporters. This went on to the next dimension with the George Floyd assassination in 2020. BLM has expanded over time as more people have been aware of the concerns and have been exposed to horrifying footage of police brutality.

## Objective

To explore and analyze the dataset and statistics of police violence in the United States. Also to predict the number of killings for a particular month which we have derived from the given dataset.

## Approach

Data mining and machine learning approaches could be used to solve this category of problems, according to a deeper examination of the problem statement. The problem essentially involves cleaning the data, visualizing and doing pre-processing for the Time series analysis, detecting whether a particular dataset is stationary in terms of time. Then training the derived dataset on a model based on stationarity and plotting the AutoCorrelation and Partial Correlation for the hyperparameters.

## Literature/Market review

- Time Series Analysis is the most explored area in the field of machine learning.
- It is not about the accuracy that we get in the Time Series Analysis, it is about the precision. Even Though the model seems to be having an accuracy of 98%. It might seem to a layman that the accuracy is too good but when this same model is applied to stock market prediction then these smaller changes on 2% can cause billions in the loss. 
- In order to achieve precision in a Time series analysis. Before moving forward with prediction,  a person needs to understand the data based on his/her own intuition. For eg. by plotting the results a person needs to figure out whether the data seems to be stationary or non-stationary by performing some test like adfuller and then move forward with choosing the best-suited model.
- Even after this, there are many factors that might result in the worst precision for a model. So for this, we just need to do hyperparameter tuning using the order term in Time series analysis.

## Algorithms used

### ARIMA Model

- The ARIMA model predicts a given time series data (which is in DateTime format) based on the past values which we have(in our case the number of kills) 
- For non-stationary data, the ARIMA model is often the best choice.
- Arima is the abbreviated version of Automated Regression Integrated Moving Average.

### SARIMAX MODEL

- The most important difference between ARIMA and SARIMAX is that in SARIMAX the model is considered to be stationary and based on that we have to do the prediction.
- But actually, our mode was non-stationary which we concluded from the Augmented Dickey Fuller test which we performed and from that we obtained the p-value less than 0.05. So the data was non-stationary.
- We converted the non-stationary data to stationary using the seasonal order of 12.

## Datasets Used

- Fatal_Encounters - 28600 rows x 29 columns ([](https://www.kaggle.com/jpmiller/police-violence-in-the-us?select=fatal_encounters_dot_org.csv))
- Police_Killings - 8427 rows x 67 columns 
([https://www.kaggle.com/jpmiller/police-violence-in-the-us/version/19?select=police_killings.csv](url))




 
