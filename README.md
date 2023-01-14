
# California Housing Prices Data

This dataset is based on data from the 1990 California census.

## Goal of this project
* Use California census data to build model of housing prices in the state.
    * The model should be able to predict the median housing price in any district, given all other metric.
    
### Data Metrics
* Population
* Median Income
* Median Housing Prices For Each Block Group
    * Block Groups are the smallest geographical unit for which the US Census Bureau sample data.
        * A Block Group typically has a population of 600 to 3,000 people.

# Framing The Problem:
* Is it  a Supervised, Unsupervised or Reinforcement Learning Problem ?
    * It is a Supervised Problem as we are given the *labeled* training data (median housing price)
* Is it a Classification task, Regression task or something else ?
    * This is a Regression task as we are to predict  a value.

# Performance Metrics
* The Performance Metrics we are using to measure our model's performance is Root Mean Square Error (RMSE). 
   * It gives us an idea of how much error the system typically makes in its predictions, with a higher weight for large errors. 
{RMSE IMAGE HERE}

# Data Distribution
{hist  here}
* The Median Income does not look like it is expressed in US dollars. It has been capped at 15 for higher median income and 0.5 for lower median income.
    * The numbers represent roughly ten thousand dollars (3 actually means $30,000)
* The housing median age and median house value were also capped.

# Creating Income Categories
{INCOME GRAPH HERE}
* Most Median Income values are clusteres around 1.5 to 6, but some median incomes go far beyond 6. 
    * We are going to create an income category with 5 categories from 1 to 5.


# Visualizing Geographical Data
{INSERT MAP}
* This image tells you that the housing prices are very much related to the location (e.g., close to the ocean) and to the population density.

# Data Correlation
{INSERT SCATTER MATRIX}
* The most  promising attribute to predict the median house value is the median income

{INSERT MEDIAN INCOME GRAPH}
* This plot reveals a few things. 
1. First, the correlation is indeed very strong; you can clearly see the upward trend, and the points are not too dispersed. 
2. Second, the price cap that we noticed earlier is clearly visible as a horizontal line at $500,000. But this plot reveals other less obvious straight lines: a horizontal line around $450,000, another around $350,000, perhaps one around $280,000, and a few more below that.