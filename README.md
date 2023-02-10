# Food-Sales-Predictions
- *Faris Assallami*
# Project 1 - Part 1

## Loading Data

from google.colab import drive
drive.mount('/content/drive')
import pandas as pd

df = pd.read_csv('/content/sales_predictions.csv')
df.info()
df.head()

print(df.isna().sum())


## Data Cleaning

# Removing columns that contain irrelevant data
df = df.drop(columns=['Item_Identifier', 'Item_Weight','Outlet_Establishment_Year'])

print("After removing 3 irrelevant columns, there are now 8523 rows and 9 columns left")
print()
df.shape
df.head()

print(df.duplicated().any())
print("There are no duplicates.")

print(df.isna().sum())
print()
print("There are 2410 missing values in the Outlet_Size column ")
print()
print()
df[df.isna().any(axis=1)]
print()
print()
print(df['Outlet_Size'].value_counts())
print()
print()


modeSize = str(df["Outlet_Size"].mode())
print()
df['Outlet_Size'].fillna(value = modeSize, inplace = True)
print(modeSize)

print(df.isna().sum())
print()
print("The Outlet_Size column no longer has missing values as seen in the chart above.")

print(df["Item_Fat_Content"].value_counts())
print()
print("--Inconsistent categories fount in Item_Fat_Content column.\n LF and low fat will be corrected to Low Fat, and reg will be corrected to Regular")
print()

df['Item_Fat_Content'] = df['Item_Fat_Content'].replace('LF', 'Low Fat')
df['Item_Fat_Content'] = df['Item_Fat_Content'].replace('low fat', 'Low Fat')

df['Item_Fat_Content'] = df['Item_Fat_Content'].replace('reg', 'Regular')

print(df["Item_Fat_Content"].value_counts())
print()
print("--All inconsistencies have been corrected.")

df

statistics =  df.describe()
statistics.loc[['mean','min','max']]


## Exploratory Visuals
## Explanatory Visuals
