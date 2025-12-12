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
S.No     &ensp;&ensp;          Date     &ensp;&ensp; &ensp;    0   &ensp;  &ensp; &ensp;    1     &ensp; &ensp;&ensp;     2   &ensp;&ensp; &ensp;   total_units\
0         &ensp;       2025-12-13 &ensp; 64.059563 &ensp; 39.325989 &ensp; 108.077087 &ensp;  211.462639\
1         &ensp;       2025-12-14  &ensp;64.051582  &ensp;45.130676 &ensp; 115.484825 &ensp;  224.667084\
2         &ensp;       2025-12-15&ensp;  64.041199&ensp;  48.390911&ensp;  120.288803  &ensp; 232.720913\
3         &ensp;       2025-12-16  &ensp;64.031914  &ensp;48.160152 &ensp; 119.907021  &ensp; 232.099087\
4         &ensp;       2025-12-17  &ensp;64.024300&ensp;  44.476101  &ensp;114.298599&ensp;   222.799000\
5          &ensp;      2025-12-18&ensp;  64.018776 &ensp; 38.297073 &ensp; 105.160355 &ensp;  207.476204\
6          &ensp;      2025-12-19 &ensp; 64.014496 &ensp; 31.517681&ensp;   95.028458 &ensp;  190.560635\
