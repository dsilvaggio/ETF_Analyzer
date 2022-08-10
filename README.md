# ETF_Analyzer
## Overview
ETF (exchange-traded fund) data was pulled from a SQL database and analyzed using Python. The Voila library was then used to create a visual web application of the analysis findings. 

### Resources/Tools
- Python
- Pandas
- SQL
- SQLAlchemy
- hvPlot
- Voila
- ETF Database

## Results
### Single Asset Analysis
Using SQL query statements, all of the PYPL data from the database was read and turned into a Pandas dataframe.
![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.00.29%20AM.png)

HvPlot was then used to create a line graph showing the PYPL daily returns. 
![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.00.54%20AM.png)

In order to find the PYPL cummulative returns, the **.cumsum()** function was first used on the daily returns column in the PYPL dataframe. HvPlot was then used again to show the cummulative returns for PYPL in a line graph. 
![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.01.01%20AM.png)


### Optimize Data Access
Advanced SQL queries were written using SQLAlchemy to optimize the efficiency of accessing data from our database. First, a query was written to obtain the time and closing price for PYPL where the closing price was greater than 200.0. The **pd.read_sql()** function was then used to turn the retrieved data into a Pandas dataframe.

![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.06.53%20AM.png)

A second query was written select the time an daily returns of the top 10 daily return values for PYPL. The **pd.read_sql()** function was used to turn the retrieved data into another Pandas dataframe.

![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.07.01%20AM.png)

### ETF Portfolio Analysis
The entire ETF portfolio was then analyzed to evaluate its performance. A SQL query was written that joined each tabled in the database into a single Pandas dataframe, using an inner join. Then **.mean()** function was then used to find the average daily returns for all four assets. This result was then stored into another dataframe. Using these averages, the annualized return was found by taking the mean of the averages dataframe, multipling this mean by 252, and then multiplying this number by 100. The result gave us an annualized return of **43.827272**.
![This is an image]()

The **.cumsum()** function was then used on the averages dataframe to create a new dataframe that stored the cummulative return values for the entire ETF portfolio.

![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.27.39%20AM.png)

Using the above cummulative returns dataframe, a final line graph was created using hvPlot to display the cummulative return values for the entire ETF portfolio.

![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.27.49%20AM.png)

## Summary
