# Product level analysis of Japan's trade statistics

 As a part of MACS30123 Large-Scale Computing for the Social Sciences, this personal project works on 
 [Japanese Trade Statistics](https://www.e-stat.go.jp/en/stat-search/files?page=1&toukei=00350300&tstat=000001013141) and conducts 
 Big Data analysis with Data Visualization and Regression. 
 
## Social Questions

Determining the factors that influence trade flows has been a prominent area of study in international financial literature (refer to [1] for an overview). One specific aspect that has garnered significant attention is the exchange rate elasticity of trade balance. Understanding this elasticity is crucial as countries often focus on currency devaluation as a means to improve their trade balance. However, empirical studies examining the J-curve effect hypothesis, which explores the trade response to devaluation in both the short and long term, have produced mixed results (refer to [2] for a review of the J-curve effect).

One of the reasons for these inconsistent findings is the reliance on aggregate export or import data in many studies. To address this issue, Bahmani-Oskooee has conducted several studies using country-specific trade data or product-level data (e.g., [3,4]). This approach allows for a more nuanced understanding of the heterogeneous effects of exchange rates.

Furthermore, the integration of the global value chain (GVC) in recent years has significantly altered the trade flow response to exchange rates. For instance, Japanese manufacturers began relocating their operations abroad during the 1990s, reducing their vulnerability to exchange rate fluctuations [5].

Building upon Bahmani-Oskooee's methodology, the objective of our study is to analyze the exchange rate elasticities at the product level using up-to-date data and detailed bicountry and product level Japanese data. 

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

[3] Bahmani-Oskooee, Mohsen, and Zohre Ardalani. 2006. Exchange Rate Sensitivity of U.S. Trade Flows: Evidence from Industry Data. Southern Economic Journal 72, no. 3 (2006): 542–59. 

[4] Bahmani-Oskooee, M., & Aftab, M. 2017. On the asymmetric effects of exchange rate volatility on trade flows: New evidence from US-Malaysia trade at the industry level. Economic Modelling, 63, 86-103.

[5] Shimizu, J., Sato, K. 2015. Abenomics, Yen Depreciation, Trade Deficit, and Export Competitiveness. RIETI Discussion Paper,15-E-020. 
