# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data for electricity production.
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
~~~
import matplotlib.pyplot as plt
import pandas as pd

# Load the data from the CSV file
df = pd.read_csv('Electric_Production.csv')
df.head()

# Convert the 'DATE' column to datetime format
df['DATE'] = pd.to_datetime(df['DATE'])

# Plotting the time series data
plt.figure(figsize=(10, 6))
plt.plot(df['DATE'], df['IPG2211A2N'], marker='o', linestyle='-', color='b')
plt.title('Electricity Production Over Time')
plt.xlabel('Date')
plt.ylabel('Electricity Production (Units)')
plt.grid(True)
plt.xticks(rotation=45)
plt.tight_layout()

# Display the plot
plt.show()

~~~










# OUTPUT:

<img width="886" alt="image" src="https://github.com/user-attachments/assets/015692f9-4a20-463f-970a-eefede81f88c">





# RESULT:
Thus the python code for plotting the time series of given data.
