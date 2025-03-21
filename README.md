## Ex.No: 01A PLOT A TIME SERIES DATA
## AIM:
To Develop a python program to Plot a time series data.
## ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
## PROGRAM:
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
![image](https://github.com/user-attachments/assets/3be9d0e3-4d8c-49c3-91d9-e04cca4d6d07)

## RESULT:
Thus we have created the python code for plotting the time series of given data.
