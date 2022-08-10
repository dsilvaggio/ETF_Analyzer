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

In order to find the PYPL cummulative returns, the .cumsum() function was first used on the daily returns column in the PYPL dataframe. HvPlot was then used again to show the cummulative returns for PYPL in a line graph. 
![This is an image](https://github.com/dsilvaggio/ETF_Analyzer/blob/main/Resources/Screen%20Shot%202022-08-10%20at%209.01.01%20AM.png)


### Optimize Data Access
### ETF Portfolio Analysis

## Summary
