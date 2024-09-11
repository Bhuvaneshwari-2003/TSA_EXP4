# Ex.No:04   FIT ARMA MODEL FOR TIME SERIES
# Date: 



### AIM:
To implement ARMA model in python.
### ALGORITHM:
1. Import necessary libraries.
   
2. Set up matplotlib settings for figure size.

3. Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000
data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

4. Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using
plot_acf and plot_pacf.

5. Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000
data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

6. Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using
plot_acf and plot_pacf.
### PROGRAM:
```
Developed by: S.bhuvaneshwari
Reg No: 212221240010
```
```
from pandas import read_csv
from pandas import datetime
from matplotlib import pyplot
from pandas.plotting import autocorrelation_plot
from pandas import DataFrame
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.arima_process import ArmaProcess
import matplotlib.pyplot as plt
import numpy as np
import warnings
warnings.filterwarnings('ignore')
import matplotlib.pyplot as plt
import numpy as np

plt.rcParams['figure.figsize'] = [10, 7.5]

ar1 = np.array([1,0.33])
ma1 = np.array([1,0.9])
ARMA_1 = ArmaProcess(ar1,ma1).generate_sample(nsample = 1000)
plt.plot(ARMA_1)
plt.title('Simulated ARMA(1,1) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_1)
plot_pacf(ARMA_1)
ar2 = np.array([1, 0.33, 0.5])
ma2 = np.array([1, 0.9, 0.3])
ARMA_2 = ArmaProcess(ar2, ma2).generate_sample(nsample=10000)
plt.plot(ARMA_2)
plt.title('Simulated ARMA(2,2) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_2)
plot_pacf(ARMA_2)
```


### OUTPUT:

# SIMULATED ARMA(1,1) PROCESS:

![image](https://github.com/user-attachments/assets/e058e52a-ba6a-4306-85b1-99788fbd7a93)


# Partial Autocorrelation

![image](https://github.com/user-attachments/assets/587f6942-8005-41f0-b657-0cc1195ae1e6)

# Autocorrelation

![image](https://github.com/user-attachments/assets/ab2d8062-7ac8-4a94-911f-32f33f9e4aaa)


# SIMULATED ARMA(2,2) PROCESS:

![image](https://github.com/user-attachments/assets/df335161-412d-40ec-8329-5340fe530c73)

# Partial Autocorrelation

![image](https://github.com/user-attachments/assets/c8492b02-9dc3-4833-9281-ececb2ebb6e5)


# Autocorrelation

![image](https://github.com/user-attachments/assets/15bbb5e2-e3f6-409c-89e0-e2ac94d6a8e6)


### RESULT:
Thus, a python program is created to fir ARMA Model successfully.
