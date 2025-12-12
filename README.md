# HCL-TECH-hackathon
## Project summary
This project builds and compares time-series forecasting models to predict daily Units_Sold for multiple product categories (Clothing, Household, Electronics). It uses a simulated retail dataset that contains a target (Units_Sold) plus macro (exogenous) and category-specific features. The goal is accurate 7-day ahead forecasting for each product category using classical and ML/Deep learning approaches. See the project brief and dataset description for details. 
## Key points from the data documentation (source)

### Target: 
Units_Sold (daily count). 
### Macro / exogenous features (shared across categories): 
Rainfall_mm (log-transformed), Avg_Daily_Temperature, Demand_Index, Is_Holiday, Is_Weekend. 
### Category-specific features: 
Product_Category, Price, Is_On_Sale. 
### Preprocessing notes: 
1)missing value handling (ffill, interpolation)\
2)label encoding for Product_Category \
3)StandardScaler applied to exogenous numerical features (target left unscaled)\
4)log transform applied to rainfall.

## Model Training
### 1) LSTM
category 0:Test MAE: 5.690, RMSE: 43.828, MAPE: 8.700%\
category 1:Test MAE: 5.797, RMSE: 66.378, MAPE: 15.995%\
category 2:Test MAE: 11.596, RMSE: 209.776, MAPE: 11.936%\
S.No               Date          0          1           2       total_units\
0         &ensp       2025-12-13 &ensp 64.059563 &ensp 39.325989 &ensp 108.077087 &ensp  211.462639\
1                2025-12-14  64.051582  45.130676  115.484825   224.667084\
2                2025-12-15  64.041199  48.390911  120.288803   232.720913\
3                2025-12-16  64.031914  48.160152  119.907021   232.099087\
4                2025-12-17  64.024300  44.476101  114.298599   222.799000
5                2025-12-18  64.018776  38.297073  105.160355   207.476204
6                2025-12-19  64.014496  31.517681   95.028458   190.560635
