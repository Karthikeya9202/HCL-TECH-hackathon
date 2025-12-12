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
missing value handling (ffill, interpolation), label encoding for Product_Category, StandardScaler applied to exogenous numerical features (target left unscaled), log transform applied to rainfall. See parsed methodology and visual diagnostics (histograms / correlation heatmap) in the provided document
