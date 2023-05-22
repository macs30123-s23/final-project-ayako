# Product level analysis of Japan's trade statistics

 As a part of MACS30123 Large-Scale Computing for the Social Sciences, this personal project works on 
 [Japanese Trade Statistics](https://www.e-stat.go.jp/en/stat-search/files?page=1&toukei=00350300&tstat=000001013141) and conducts 
 Big Data analysis with Data Visualization and Regression. 
 
## Social Questions

 The determinant of trade flows have been the most interested topics in International Financial literatures (see [1] for overview). 
 Specifically, the exchange rate elasticity to trade balance has been actively investigated over the past years. The exchange elasticity matters 
 because countries pay an extensive attention to devaluation of currency and thereby the improvement of trade balance. However, the J-curve effect hypothesis, 
 which states the trade response to devaluation in short and long-term, has empirically mixed results (see [2] for J-curve effect's review). 
 As 

## Dataset
 
* Trade Statistics
  Update Kaggle dataset with recent data. Monthly level data from 1988-2020 and most granular product level ([HS9 codes](https://www.trade.gov/harmonized-system-hs-codes)). 
    * [Kaggle 1988-2020](https://www.kaggle.com/datasets/zanjibar/100-million-data-csv)
    * [E-Stat](https://www.e-stat.go.jp/en/stat-search/files?page=1&toukei=00350300&tstat=000001013141): scarped with [API](https://www.e-stat.go.jp/api/en)
* Exchange Rates
  Downloaded quarter data of "National Currency Per U.S. Dollar, Period Average Rate" from [IMF](https://data.imf.org/?sk=4c514d48-b6ba-49ed-8ab9-52b0c1a0179b&sId=1390030341854). 
* GDP
  Downloaded quarter data of "Nominal, Domestic Currency, Seasonally Adjusted GDP" from [IMF](https://data.imf.org/?sk=4c514d48-b6ba-49ed-8ab9-52b0c1a0179b&sId=1390030341854). 
  
Since their is a mismatch between country codes between trade dataset and IMF dataset, we used `fuzzywuzzy' to match country names. 

## References

[1] Krugman, P., Obstfeld, M., Melitz, M. 2018. International Economics: Theory and Policy. Pearson Education Limited. 

[2] Bahmani-Oskooee, M., and Ratha, A. 2004. The J-curve：a literature review. Applied economics, 36(13), 1377–1398.

[3] Bahmani-Oskooee, M., & Aftab, M. 2017. On the asymmetric effects of exchange rate volatility on trade flows: New evidence from US-Malaysia trade at the industry level. Economic Modelling, 63, 86-103.
