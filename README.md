Demand Forecasting & Inventory Optimization

This project focuses on improving demand forecasting and using the forecast results to make better inventory decisions.

The main idea was to compare different forecasting methods, identify the best-performing model, and then study how better forecasting can affect safety stock, reorder points and inventory holding costs.

I worked with four forecasting approaches:

• Naive
• SARIMA
• Holt-Winters
• XGBoost

XGBoost gave the best forecasting performance with a MAPE of 13.3%, compared with 19.9% for the Naive model.

The forecasting results were then used for inventory optimization at a 95% service level.

Some of the main results were:

• 33.3% reduction in safety stock
• 5.3% reduction in holding cost
• Approximately ₹7.29 lakh annual holding cost saving
• Safety stock reduced from 25,117 units to 16,746 units

I also tested the models using an empirical stockout-risk backtest. One interesting finding was that XGBoost had a higher stockout rate than the Naive model even though its MAPE was much better.

Naive stockout rate: 4.12%
XGBoost stockout rate: 5.55%

This showed that better forecast accuracy does not always mean better operational performance. A small positive forecast bias in the XGBoost predictions contributed to the higher stockout rate. I kept this result as it was instead of applying a correction just to improve the final numbers.

The project was developed using Python, Pandas, NumPy, Scikit-learn, XGBoost, SQL/SQLite and Power BI.

The project includes:

• Five Jupyter/Google Colab notebooks covering the complete analysis
• Final Power BI dashboard
• Validated CSV outputs used for the dashboard
• Dashboard screenshots

The Power BI dashboard is divided into five pages:

1. Executive Overview
   Main project KPIs and overall results.

2. Forecast Accuracy Analysis
   Comparison of actual and forecast demand, model MAPE and ABC-class performance.

3. Inventory Optimization
   Comparison of safety stock, reorder points and holding costs between the two policies.

4. Service Level Analysis
   Shows how safety stock and holding cost change as the service level increases from 90% to 99%.

5. Stockout Risk Analysis
   Compares Naive and XGBoost stockout rates at store and SKU level.

The final data was validated after export so that the numbers shown in Power BI could be independently reproduced from the CSV files.

Key results at a glance:

XGBoost MAPE: 13.3%
Naive MAPE: 19.9%
Safety stock reduction: 33.3%
Holding cost reduction: 5.3%
Annual saving: ₹7.29 lakh
Naive stockout rate: 4.12%
XGBoost stockout rate: 5.55%

Dashboard screenshots:

Executive Overview

![Executive Overview](images/page1_executive_overview.png)

Forecast Accuracy

![Forecast Accuracy](images/page2_forecast_accuracy.png)

Inventory Optimization

![Inventory Optimization](images/page3_inventory_optimization.png)

Service Level Analysis

![Service Level Analysis](images/page4_service_level_analysis.png)

Stockout Risk

![Stockout Risk](images/page5_stockout_risk.png)

Project structure:

notebooks/
Contains the five notebooks used for data preparation, forecasting, inventory optimization and validation.

powerbi/
Contains the final Power BI dashboard.

images/
Contains screenshots of all five dashboard pages.

exports/
Contains the final validated CSV files used as inputs for Power BI.

Tools used:

Python
Pandas
NumPy
Scikit-learn
XGBoost
SQL / SQLite
Google Colab
Power BI
DAX
Excel

This project helped me understand how forecasting, inventory planning and business analytics are connected, and also showed me why a forecasting model should be evaluated using business and operational outcomes rather than accuracy metrics alone.

Kaushik Gupta
