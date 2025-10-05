# Colina-2ECEA-PA3(PYTHON DATA ANALYSIS (PANDAS))

## Objectives
1.To identify the codes and functions incorporated in the Pandas library 

2.To be able to apply and use the different codes and functions in creating a Python program using a 
Pandas library

## Problem 1:Loading of csv

So we are tasked to:
1. Load the corresponding .csv file into a data frame named cars using pandas
2. Display the first five and last five rows of the resulting cars.

Steps:

Before we start we must import pandas

```python
import pandas as pd
```

1.To load the csv file we need to type pd.read_csv('file name'.csv) in our case:

```python
df=pd.read_csv('cars.csv')
df
```

This will show the data of cars.csv:

2.To load the first and last 5 rows of the resulting cars we need to use the function head and tail like this:

1st 5 rows:

`
df.head()
`

This will show the 1st 5 rows of the selected vehicle(the default number of the parenthesis is 5).Resulting to:

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/154a7fe2-2436-4c3d-9381-55414a7cd262" />

Last 5 rows:

`
df.tail()
`

This will show the last 5 rows of the selected vehicle.Resulting to:

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/7b606591-536e-48b2-9c98-8386e4ae0a37" />

## Problem 2:Subsetting,Slicing,and Indexing operations

So we are tasked to:

1.Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7…) of cars. 

2.Display the row that contains the ‘Model’ of ‘Mazda RX4’.

3.Display how many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?

4.Display how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

Steps:

1.To display the five rows with odd-numbered columns we need the function iloc because it selects single value by row and column.

`
odd_columns = df.iloc[:5, ::2]
odd_columns
`

The :5 selects the number of rows and the ::2 skips every other column starting 0

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/66aa8bbf-3474-4a53-b0bc-ac6d0990984b" />

2.To select the row with the Mazda RX4 we need to identify which category it falls into(Model)

`
Rows=df[df['Model'] == 'Mazda RX4']
Rows
`

This will show the statistics of the model Mazda RX4:

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/4986c386-fde3-463f-a563-be1cc0707460" />

3.To get the number of cyl of the model:Camaro Z28. We need to use the function .loc[].

`
cyl = df.loc[df['Model'] == 'Camaro Z28',['Model','cyl']]
cyl
`

The right side will only display the model and the cyl nothing else

<img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/382eeb80-4f84-4704-8072-e795c0d81349" />

4.To determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have. We need to use the function .loc[] and use .isin() since we need to get multiple car models.

`
cyl_gear = df.loc[df['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']),['Model','cyl', 'gear']]
cyl_gear
`

Then it will display our selected model,cyl, and gear:

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/f0c486d4-e627-4cf8-9206-4df217144fc0" />
