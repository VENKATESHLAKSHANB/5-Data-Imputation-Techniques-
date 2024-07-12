# 5-Data-Imputation-Techniques-
*Mean/Median Imputation*

 import pandas as pd
 import numpy as np
 # Load the dataset
 df = pd.read
 csv ( ’ecommerce data. csv ’)
 # Impute missing ages with mean
 df [ ’age ’ ]. fillna (df [ ’age ’ ].mean() , inplace=True)

 *Multiple Imputation*
 from sklearn . experimental import enable iterative imputer
 from sklearn .impute import IterativeImputer
 import numpy as np
 # Assuming ’lab results ’ is our dataset with missing values
 imputer = IterativeImputer(random
 imputed
 state=0)
 data = imputer. fit transform( lab)

 *K-Nearest Neighbors (KNN) Imputation*
 from sklearn .impute import KNNImputer
 imputer = KNNImputer(n
 neighbors=5)
 housing data imputed = imputer. fit transform(housing data)



*Regression Imputation*
 from sklearn . linear model import LinearRegression
 # Assume X
 ’ years of train has complete cases , y train is experience ’
 reg = LinearRegression (). fit (X train , y train )
 # Predict missing ’years of experience ’
 df . loc [ df [ ’ years of experience ’ ]. isnull () , ’ years of experience ’ ] = \
 reg . predict (df . loc [ df [ ’ years of experience ’ ].isnull () , X
 train . columns ])

*Time Series Imputation*
 import pandas as pd
 # Assume ’stock data ’ is a time series of stock prices
 stock data imputed = stock
 data . interpolate (method=’time ’
