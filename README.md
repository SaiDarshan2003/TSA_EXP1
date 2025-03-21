# Ex.No: 01A PLOT A TIME SERIES DATA
# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
## PROGRAM DEVELOPED BY: LOKESH R
## REG NO: 212222240055
## PROGRAM:
## POPULATION:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
## OUTPUT:
## POPULATION:

![pop](https://github.com/LokeshRajamani/TSA_EXP1/assets/120544804/5fe0a8f5-4301-451d-8129-d471a27595a4)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
