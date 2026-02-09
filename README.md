# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df = pd.read_csv("BMW_Data.csv")
df.head()
df['Date'] = pd.to_datetime(df['Date'], errors='coerce')
df.set_index('Date', inplace=True)

print(type(df.index))  # Should show DatetimeIndex
df.head()
plt.figure(figsize=(12,6))
plt.plot(df['Volume'])
plt.title("Original Time Series (Volume)")
plt.xlabel("Date")
plt.ylabel("Volume")
plt.grid(True)
plt.show()
```











# OUTPUT:

<img width="1001" height="547" alt="image" src="https://github.com/user-attachments/assets/3eba8307-4e60-4651-a514-52e46ff2e10c" />







# RESULT:
Thus we have created the python code for plotting the time series of given data.
