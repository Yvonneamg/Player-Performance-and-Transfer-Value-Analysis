# Player-Performance-and-Transfer-Value-Analysis

# Data
The data for this repository is obtained from 2 sources from Kaggle.
1. [Premier League Player Statistics 23/24](https://www.kaggle.com/datasets/orkunaktas/premier-league-all-players-stats-2324) It contains players statistics in the season 2023/24 when Manchester City became champions. The data set has `34 columns` and `581 rows`.
2. [Football Transfer Data](https://www.kaggle.com/datasets/khanghunhnguyntrng/football-players-transfer-fee-prediction-dataset). It contains transfer statistics of 11 european leagues, 4 american leagues, 4 asian leagues and one african league inclusive of player statistics in the seasons 2021/2022 and 2022/2023. The data has `22 columns` and `10,755 rows`.

# Tools
- Power Query
- Power Pivot
- Excel

**Power Query**:
- We will use power query to export, transform and load the data to excel and power pivot.
- We first load the data to power query. Change each column data type to ensure you have the right data type say `text`,`whole number` or `decimal number` accordingly. We do this for both sets of datasets.
- Proceed to merge the queries in power query and choose the columns we want to obtain from the second table. In our case, I used a left join with the premier league player statistics 2023/24 as the first table and Football transfer data as the second table. I used a fuzzy match with a similarity ratio of 0.8 to accommodate the different accents on the player names.
- Close and load the data as a connection and add it to the data model.

**Power Pivot**:
- From power pivot, create a calculated column called Performance score. Multiply the players goals by 0.5, the assists by 0.3 and the minutes played by 0.2 to create a simplified model.
