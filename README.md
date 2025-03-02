# ONLINE-RETAIL-STORE-ANALYSIS

## TABLE OF CONTENT
- [Introduction](#Introduction)
- [Dataset Overview](#Dataset-Overview)
- [Data Quality Assessment](#Data-Quality-Assessment)
- [Tools & Technology Used](#Tools-&-Technology-Used)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Feature Engineering](#Feature-Engineering)
- [Visualization](#Visualization)
- [Clustering Analysis](#Clustering-Analysis)
- [Predictive Classification Model](#Predictive-Classification-Model)
- [Sales Forecasting](#Sales-Forecasting)
- [Customer Segmentation](#Customer-Segmentation)
- [Business Insights & Marketing Strategy Recommendation](#Business-Insights-&-Marketing-Strategy-Recommendation)
- [Conclusion](#Conclusion)
- [Recommendation](#Recommendation)

## INTRODUCTION

### Objective

The purpose of this project is to design a predictive model that categorizes online shopping transactions into certain categories and clusters. Utilizing machine learning and clustering techniques, the model will help businesses identify hidden patterns, reduce inventory management complexities, improve customer segmentation, and enhance sales forecasting.

## DATASET OVERVIEW
The dataset used in this project is online retail transactions and contains the following primary columns:

- **InvoiceNo**: Unique transaction code.
- **StockCode**: Unique product code.
- **Description**: Name of product.
- **Quantity**: Units purchased.
- **InvoiceDate**: Date and time of transaction.
- **UnitPrice**: Cost per unit of product.
- **CustomerID**: Unique customer code (few missing values).
- **Country**: Country in which transaction was made.

## DATA QUALITY ASSESSMENT
## Identified Issues

**Missing Values**:

- 1,454 missing values in the Description column.
- 135,080 missing values in the CustomerID column.

**Negative Values**:

- 10,624 negative values in the Quantity column (indicating product returns).
- 2 negative values in the UnitPrice column.

**Zero Values**:

- 2,515 zero values in the UnitPrice column.

**Special Characters and Blanks**:
- Special characters and blank values in the Description column.

**Duplicate Rows**:

- 5,268 duplicate rows.

**Unspecified Entries**:

- Some rows in the Country column had "unspecified" entries.

## Rectified Issues
**Handling Missing Values**:

- CustomerID: Missing values were handled using forward fill.
- Description: Missing values were identified and handled.

**Removing Negative and Zero Values**:

- Classified negative Quantity values as product returns.
- Removed negative UnitPrice values they identify possible debt and invalid entries.
- Filtered out zero UnitPrice values.

**Renaming "Unspecified" Country**:

- "Unspecified" country entries were renamed to "Unknown" for clarity.

**Removing Duplicates:**

- Dropped 5,268 duplicate rows to ensure data accuracy.

**Standardizing Product Descriptions:**

- Renamed the Description column to Product for consistency.

## TOOLS AND TECHNOLOGIES

- **Excel** for initial data exploration and anomaly detection.
- **Python** (pandas, numpy, matplotlib, seaborn, scikit-learn, XGBoost, Prophet).
- **Jupyter Notebook** for visualization and analysis.
- **Machine Learning Models**:Random Forest
- **Clustering Techniques:** K-Means Clustering.
- **Time Series Analysis:** Facebook Prophet to predict sales.

## EXPLORATORY DATA ANALYSIS (EDA)

## FEATURE ENGINEERING

**Created new features:**

- Total Sales
- Year
- Quarter
- Month
- Hour of the Day
- Period of the Day
- Days of the Week





#### 5. Predictive Classification Model

  - Implemented machine learning models (Logistic Regression, Random Forest, XGBoost).
  - Trained models to classify transactions based on customer purchasing behavior.
  - Evaluated performance using accuracy, precision, recall, and F1-score.

#### 6. Clustering Analysis

  - Used unsupervised learning (K-Means) to segment customers based on shopping patterns.
  - Determined optimal clusters using the Elbow method and silhouette score.

#### 7. Sales Forecasting (Time Series Analysis)

  - Applied Facebook Prophet to predict future sales trends.
  - Evaluated forecast accuracy using RMSE and MAPE.
  - Provided insights into expected revenue trends for strategic decision-making.

## TOOLS AND TECHNOLOGIES

- Python (pandas, numpy, matplotlib, seaborn, scikit-learn, XGBoost, Prophet)
- Jupyter Notebook for data analysis and visualization
- Machine Learning Models: Decision Trees, Random Forest, XGBoost, Logistic Regression
- Clustering Techniques: K-Means Clustering
- Time Series Analysis: Facebook Prophet for sales forecasting

## EXPLORATORY DATA ANALYSIS (EDA)

### Summary Statistics and Data Insights

- Identified sales trends over time (yearly, quarterly, and monthly patterns).
- Examined customer purchase behavior based on days of the week and times of the day.
- Visualized top-selling products and purchase frequency.
- Analyzed customer retention based on Recency, Frequency, and Monetary (RFM) metrics.

## FEATURE ENGINEERING

- Created new features:
  - Total Sales = Quantity Sold × Unit Price
  - Purchase Period: Morning, Afternoon, Evening classification
- Days of the Week Analysis
- Outlier Detection and Handling: Used IQR method to remove anomalies.
- Feature Scaling & Encoding: Standardization and categorical variable encoding.

## PREDICTIVE CLASSIFICATION MODEL

### Machine Learning Models Used:
  - Logistic Regression
  - Random Forest
  - XGBoost
  - 
### Model Evaluation:
  - Accuracy, Precision, Recall, F1-score
  - Feature importance analysis
  - Addressed class imbalance with resampling techniques

## CLUSTERING ANALYSIS

### Customer Segmentation (K-Means Clustering)
  - Performed RFM Analysis:
    - Recency: How recently a customer purchased
    - Frequency: How often a customer buys
    - Monetary Value: How much a customer spends
    
### Segmented Customers into Groups:
  - High-Value Customers
  - Regular Buyers
  - One-Time Shoppers
  - Visualized Customer Clusters to understand patterns and marketing opportunities.

## SALES FORECASTING
Time Series Forecasting using Facebook Prophet
Trained model on historical sales data to predict future revenue.
Created future time periods and forecasted sales for the next months.
Visualized forecast trends with confidence intervals.
Evaluated Model Accuracy using RMSE and MAPE.
CUSTOMER SEGMENTATION REPORT
Identified key customer groups based on spending habits.
Developed tailored marketing strategies for each segment.
Recommended inventory adjustments to align with high-demand periods.
BUSINESS INSIGHTS & MARKETING STRATEGY RECOMMENDATIONS
Personalized marketing strategies based on customer segments.
Dynamic pricing and discounting strategies to maximize revenue.
Inventory restocking recommendations based on predictive insights.
Customer loyalty programs to retain high-value customers.
CONCLUSION
Data-driven insights enable businesses to optimize their sales strategies.
Predictive modeling improves transaction classification and inventory management.
Clustering analysis helps in precise customer targeting for marketing efforts.
Sales forecasting provides future revenue estimates for better planning.
RECOMMENDATIONS
Target High-Value Customers: Offer loyalty rewards and exclusive promotions.
Stock Management Optimization: Reduce overstocking and maintain high-demand product availability.
Improve Marketing Campaigns: Personalize recommendations based on customer clusters.
Monitor Sales Trends: Use sales forecasting insights for proactive decision-making.
Enhance Customer Retention: Identify at-risk customers and implement engagement strategies.
About
No description, website, or topics provided.
Resources
 Readme


