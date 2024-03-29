# Food-Sales-Predictions
- *Author: Faris Assallami*

![175866422-c6ba097d-fadb-4adc-a77e-9140cd3dd8aa](https://github.com/farisassallami/Food-Sales-Predictions/assets/111199631/ede51e57-0558-4170-b795-3da4d6d41c32)

#  Business Problem

How can we use Data Visualizations and Machine Learning techniques to analyze food sales data and identify patterns and trends that can help businesses predict and improve sales in their supermarkets and grocery stores, ultimately increasing revenue and customer satisfaction?


#  Loading Data

Loaded the csv file into colab

# Data Cleaning

Removed irrelevant columns that dont add any insight to the data.  Removed duplicate rows.  Filled in missing data with most frequent value.  Corrected inconsistencies and spelling errors in the data.

# Exploratory Visuals

## Using a histogram to inspect Item outlet sales

 
![histogram](https://user-images.githubusercontent.com/111199631/224218812-cf6aaeea-a789-4c94-8614-d359dbacad95.png)

 According to the histogram below we can see that the bulk of the 
 item outlet sales were valued below $2,000
 
 
---------------------------------------------

## Correlation Heat map

![heatmap](https://user-images.githubusercontent.com/111199631/224219438-1671d257-eebc-4ea2-b6e9-37f0fe69adf4.png)

We can see there is only a moderate correlation between Item MRP and The Item outlet Sales 
 We can see that Item visibility and item weight have almost no relationship with the other variables in our data set.
 
 
# Explanatory Visuals

## Which Outlet type grossed more in sales on average?


![barplot](https://user-images.githubusercontent.com/111199631/224219702-09f01a96-aef0-447d-a6ee-7b131977d6ab.png)

We can see that Supermarket Type 3 on average Grossed more sales than all other outlet types. 

---------------------------------------------


## Does Item MRP affect sales?

![scatter](https://user-images.githubusercontent.com/111199631/224219839-30e50a76-26ed-426c-9b86-a5dcd3f3f7b7.png)

We can see that there is a positive relationship between sales and Item MRP. As additional unit of resource is added to the item, it increases its marginal value thus increasing in sales revenue.


---------------------------------------------


## What are the top 3 and bottom 3 selling categories?

![last](https://user-images.githubusercontent.com/111199631/224219985-69bae4f1-a76c-4988-8f7e-844c4b6e4b04.png)

The top 3 selling categories are:
Starchy Foods
Seafood
Fruits and Vegetables

The lowest 3 selling categories are:
Soft Drinks & Health/Hygiene
Baking Goods
Others

# Machine Learning
## ---Metrics for Linear Regression Model---

               -- Train data-- 
 R2: 0.561  
 
 MSE: 1300339.29   
 
 RMSE:1140.32  
 
 MAE:847.25

                --Test data-- 
 R2: 0.566   
 
 MSE: 1198492.81  
 
 RMSE:1094.75  
 
 MAE:805.86


---------------------------------------------

## ---Metrics for Random Forrest Model---

               --Train data-- 
 R2: 0.611   
 
 MSE: 1152591.90   
 
 RMSE:1073.58   
 
 MAE:755.37

               --Test data-- 
 R2: 0.603   
 
 MSE: 1096246.03   
 
 RMSE:1047.01  
 
 MAE:728.38
 
 --------------------------------------------
 
-For the linear regression model, We can see that Test data has a slightly higher R-squared while Train data has a slightly higher RMSE

-For the random forrest model, We can see that the Training data had both a higher R-squared and RMSE and the Testing data

Comparing both the models, I will select the Random Forrest Tree model since it has a higher R-squared than the Linear Regression model. Random Forrest models are powerful and include individual decision trees by combining dozens or hundreds of them.

-----------------------------------------------

# Recomendations

Focus on Supermarkets tier 3 since thats where the majority of the sales take place.  Customers prefer to "one-stop shop" at super centers and get all the things they need in one go.

Bulk of Item outlet sales were valued at $2,000 or below, these can be sales from staples and convient goods such as Dairy, Canned goods, Frozen foods, Fresh produce and Snack foods.

Top 3 selling categories all fresh foods.  Produce, Starchy foods, and Seafood.  It would be a great idea to have a fresh seafood boil, or juice bar for the produce as customers trend to more healthier options. 


