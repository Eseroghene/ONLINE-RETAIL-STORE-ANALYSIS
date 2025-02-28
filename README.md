# ONLINE-RETAIL-STORE-ANALYSIS

## TABLE OF CONTENT
- [Introduction](#Introduction)
- [Tools & Technology Used](#Tools-&-Technology-Used)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Feature Engineering](#Feature-Engineering)
- [Predictive Classification Model](#Predictive-Classification-Model)
- [Clustering Analysis](#Clustering-Analysis)
- [Sales Forecasting](#Sales-Forecasting)
- [Customer Segmentation](#Customer-Segmentation)
- [Business Insights & Marketing Strategy Recommendation](#Business-Insights-&-Marketing-Strategy-Recommendation)
- [Conclusion](#Conclusion)
- [Recommendation](#Recommendation)

## INTRODUCTION

### 1. Objective

The purpose of this project is to design a predictive model that categorizes online shopping transactions into certain categories and clusters. Utilizing machine learning and clustering techniques, the model will help businesses identify hidden patterns, reduce inventory management complexities, improve customer segmentation, and enhance sales forecasting.

### 2. Business Problem
Understanding customer buying behavior enables businesses to make data-driven decisions. The key objectives are:
- Customer Segmentation: Grouping customers for targeted marketing strategies.
- Inventory Optimization: Stocking high-demand products efficiently while avoiding overstocking of low-demand products.
- Revenue Growth: Forecasting future sales trends to improve decision-making.
- Marketing Strategies: Personalized recommendations and promotional campaigns based on purchasing behavior.

### 3. Methodology
A structured data science approach was followed, including:

#### 1. Data Collection & Preprocessing

  - Gathered transactional data from the online retail store.
  - Cleaned missing values, handled duplicates, and removed outliers.

#### 2. Exploratory Data Analysis (EDA)

  - Analyzed purchase trends over time (yearly, quarterly, monthly).
  - Identified top-selling products and customer purchase behavior.
  - Used visualizations to uncover sales patterns.

#### 3. Feature Engineering

  - Created new features (e.g., Total Sales, Purchase Period, Days of the Week).
  - Applied encoding techniques for categorical variables.
  - Normalized and standardized numerical data for better model performance.

#### 4.Customer Segmentation (Using RFM & Clustering)

  - Performed Recency, Frequency, and Monetary (RFM) analysis.
  - Applied K-Means clustering to group customers into meaningful segments.
  - Visualized and interpreted customer clusters.

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
Python (pandas, numpy, matplotlib, seaborn, scikit-learn, XGBoost, Prophet)
Jupyter Notebook for data analysis and visualization
Machine Learning Models: Decision Trees, Random Forest, XGBoost, Logistic Regression
Clustering Techniques: K-Means Clustering
Time Series Analysis: Facebook Prophet for sales forecasting
EXPLORATORY DATA ANALYSIS (EDA)
Summary Statistics and Data Insights
Identified sales trends over time (yearly, quarterly, and monthly patterns).
Examined customer purchase behavior based on days of the week and times of the day.
Visualized top-selling products and purchase frequency.
Analyzed customer retention based on Recency, Frequency, and Monetary (RFM) metrics.
FEATURE ENGINEERING
