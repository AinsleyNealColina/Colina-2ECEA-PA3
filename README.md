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

1.To load the csv file we need to type pd.read_csv('file name'.csv) in our case:

`
df=pd.read_csv('cars.csv')
df
`

This will show the data of cars.csv:

2.To load the first and last 5 rows of the resulting cars we need to use the function head and tail like this:

1st 5 rows:

