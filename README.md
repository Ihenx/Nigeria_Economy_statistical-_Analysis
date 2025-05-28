# Nigeria Economic Analysis (1999–2018)
Since Nigeria's return to democracy in 1999, its economy has been shaped by global oil prices, policy decisions, and governance styles under two main political parties: the People's Democratic Party (PDP) and the All Progressives Congress (APC).
Under PDP (1999–2015), the economy experienced relative growth, driven by debt relief, privatization, and a booming oil sector. Obasanjo's reforms and Jonathan's economic liberalization helped grow GDP, but inflation remained a recurring challenge, especially during oil price shocks.
Under APC (2015–present), the economy has been marked by recession (2016, 2020), currency devaluation, rising inflation, and controversial policies like border closures and subsidy removals. While reforms under Buhari and Tinubu aim for long-term stability, inflation has surged amid economic adjustments.
This project will analyze how both administrations influenced Nigeria's inflation rate using statistical and time series methods, providing insights into policy impacts over time.
## 📁 Features

- Time-series modeling using **ARIMA/SARIMAX**
- Statistical tests (t-tests) for administrative comparisons
- Forecasting inflation and GDP trends
- Visualization of economic sector contributions (Agriculture, Industry, Services)
- Correlation and autocorrelation analysis
- Clean and reproducible code with documented findings

## Introduction To Dataset
| Name              | Description                                        |
|-------------------|----------------------------------------------------|
| Inflation rate    | Annual percentage change in consumer prices       |
| Unemployment      | Percentage of the labor force without jobs        |
| Government debt   | Total public debt as a percentage of GDP          |
| Agriculture       | GDP contribution from the agricultural sector     |
| Industry          | GDP contribution from the industrial sector       |
| Services          | GDP contribution from the services sector         |
| GDP (Basic Prices)| GDP at 2010 constant basic prices (excluding taxes)|
| Net Taxes         | Taxes on products net of subsidies                |
| GDP (Market Prices)| GDP at 2010 constant market prices (includes taxes)|


## Libraries Used
To begin the analysis, essential Python libraries were imported for data loading, transformation, visualization, and modeling. Warnings were suppressed to maintain readability during iterative data exploration and statistical modeling.
```
  import pandas as pd
  import matplotlib.pyplot as plt
  import numpy as np
  import seaborn as sns
  from datetime import datetime
  from warnings import filterwarnings, filters
  filterwarnings('ignore')
```
The economic dataset is successfully loaded into a Pandas DataFrame with the following characteristics:

* Type: pandas.core.frame.DataFrame

* with about 34 annual entries ranging from 1990 to 2023

* Columns: 9 numerical features representing key macroeconomic indicators

* Non-null entries: All columns are complete (no missing data)

* Data Types: All columns are of type float64, suitable for quantitative and statistical analysis


This line of code uses label-based slicing on the DatetimeIndex to extract data from January 1, 1999 onward, effectively filtering the DataFrame to contain only the democratic period in Nigeria's Fourth Republic.
```
economic_data = econ_df.loc['1999':]
```
To maintain political and economic coherence, the analysis is limited to Nigeria's democratic era, beginning in 1999 with the transition from military to civilian rule. By slicing the dataset accordingly, we focus the investigation on economic trends, policies, and impacts under democratic administrations (PDP and APC), ensuring relevance to governance-related comparisons.



