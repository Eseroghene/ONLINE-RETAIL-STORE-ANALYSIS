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

## VISUALIZATION AND INSIGHTS

**Best-Selling Products: Total Sales & Quantity**

- Top-selling products: REGENCY CAKESTAND 3 TIER & PAPER CRAFT, LITTLE BIRDIE

- High revenue but lower quantity sold: REGENCY CAKESTAND 3 TIER – premium pricing

- High quantity but lower revenue: WHITE HANGING HEART T-LIGHT HOLDER, RABBIT NIGHT LIGHT – low-cost, bulk-sold items

- Balanced performer: MEDIUM CERAMIC TOP STORAGE JAR – strong in both sales & quantity

- Stocking strategy: Prioritize high-revenue products, optimize pricing for bulk-sellers, bundle festive & home decor items
<img width="741" alt="Best Selling Product" src="https://github.com/user-attachments/assets/fb80d4e9-c096-4d64-9f00-f20cc91d5ef0" />

**Top 10 Countries by Sales**

- Dominant Market: United Kingdom has overwhelmingly the highest sales, far exceeding all other countries.

- Other Key Markets: Netherlands, EIRE (Ireland), Germany, and France follow, but with significantly lower sales.

- Global Reach: Sales extend beyond Europe to countries like Australia, Japan, and Switzerland.

- Potential Focus Areas: Expanding marketing efforts in top-performing international markets could drive more growth.

<img width="788" alt="Screenshot 2025-03-02 at 10 36 02 AM" src="https://github.com/user-attachments/assets/af847cc7-a2ab-40b2-aa4a-6922c8cb4144" />

**Daily Purchase Trend**

- Highest sales occur on Tuesday and Thursday, with peaks above 2 million.

- Sales drop significantly on Saturday, reaching near zero, which suggests minimal or no transactions on this day.

- Sales slightly recover on Sunday but remain lower compared to weekdays.

- Overall, weekdays have higher sales than weekends, indicating that most transactions happen during the workweek.

<img width="696" alt="Screenshot 2025-03-02 at 10 37 30 AM" src="https://github.com/user-attachments/assets/3bf747ae-ad78-45e5-ab10-609886a13119" />

**Period Of The Day Purchase Trends**

- Afternoon has the highest sales, peaking around 6 million.

- Morning follows closely, with sales above 4 million.

- Sales drop significantly in the evening, suggesting fewer transactions.

- Night has the lowest sales, almost negligible, indicating little to no business activity.

<img width="688" alt="Period Of the day" src="https://github.com/user-attachments/assets/cb2904ff-33b9-45fc-a3b7-082cfa31fdd9" />

**Monthly Purchase Trend**

- Slow Start: Sales are relatively low in January and February, with fluctuations in the first half of the year.

- Steady Growth: Sales pick up from May to August, though with slight variations.

- Peak Season: Significant sales increase from September onward, peaking in November and December—likely due to holiday shopping.

- Possible Strategy: Capitalizing on peak months (November-December) with promotions and stock optimization could maximize revenue.

<img width="711" alt="Screenshot 2025-03-02 at 10 43 26 AM" src="https://github.com/user-attachments/assets/9fe01003-7d1c-4f14-b2c8-6d8ba0c372c0" />

**Quarter of the year trend**

- Gradual Growth: Sales increase steadily from Q1 to Q3, indicating a consistent upward trend.

- Major Surge in Q4: A sharp rise in Q4 sales, likely due to holiday shopping (Black Friday, Christmas).

- Strategic Focus:

  - Boost marketing and inventory for Q4 to maximize sales.
  - Identify ways to improve performance in Q1 and Q2 (e.g., 
    seasonal promotions).
  
<img width="701" alt="Screenshot 2025-03-02 at 10 44 32 AM" src="https://github.com/user-attachments/assets/0cda61ee-8a91-4773-99e5-30ba590b9880" />

## CLUSTERING ANALYSIS
- Used unsupervised learning (K-Means) for Customer Segmentation and Product Segmentation.

## Customer Segmentation
**Using The RFM Method To Check Customer Behaviour**

  - Recency(R): Measures how recently a customer made a purchase.
  - Frequency(F): Measures how often a customer makes a purchase.
  - Monetary Value(M): Measures how much money a customer has spent.
    
**Selecting And Standardizing The Clustering Features**

  - Feature Selection:- We select "Recency," "Frequency," and "Monetary Value" as they best represent customer purchasing behavior.
  - Standardization:Since the features are on different scales we use StandardScaler to normalize the data.This ensures fair distance calculations in             clustering algorithms

**Finding The Optimal Number Of Clusters**

  - Clustering requires selecting the right number of clusters (K) for the best customer segmentation.
  - Elbow Method:** Determines the ideal number of clusters by analyzing inertia (WCSS).
  - Optimal K:Identified at the "elbow point," where adding more clusters shows minimal improvement

<img width="693" alt="Screenshot 2025-03-02 at 10 52 30 AM" src="https://github.com/user-attachments/assets/c3902a12-550b-4667-8cbc-8cd567e58497" />

**Customer Segments and Strategies** After applying clustering, customers were grouped into three segments based on their purchasing behavior:

**Segment 0 (Low-Value, Infrequent Shoppers):**

- Low total sales, long time since last purchase, and low purchase frequency.
- Likely one-time or rarely active customers.
- Strategy: Re-engagement campaigns, discounts, and loyalty programs.

**Segment 1 (Medium-Value, Frequent Shoppers)**

- Moderate sales, recent purchases, and medium-to-high purchase frequency.
- Active customers who shop regularly but don't spend excessively.
- Strategy: Upselling, bundles, and membership perks to boost spending.

**Segment 2 (High-Value, Frequent & Loyal Shoppers)**

- Highest sales, very recent purchases, and extremely high frequency.
- Loyal, high-spending customers.
- Strategy: Exclusive VIP rewards, personalized offers, and premium services.

<img width="839" alt="Screenshot 2025-03-02 at 10 55 32 AM" src="https://github.com/user-attachments/assets/63f730b6-1770-4d2d-8876-0acc7391f5fe" />

## Product Segmentation
**Using Key Metrics to Group Products**

- Quantity: Measures the total number of units sold for each product.
- Total Sales: Measures the total revenue generated by each product.
- ASP (Average Selling Price): Measures the average price at which a product is sold.

**Selecting And Standardizing The Clustering Features**

- Feature Selection: We use Quantity, Total Sales, and ASP as they provide a comprehensive view of product performance.
- Standardization: Since these features have different scales, we apply StandardScaler to normalize the data, ensuring fair clustering.

**Finding The Optimal Number Of Clusters**

- Clustering helps categorize products into different segments for better pricing and sales strategies.
- Elbow Method: Determines the best number of clusters by analyzing inertia (WCSS).
- Optimal K: Identified at the "elbow point," where adding more clusters provides minimal improvement.

<img width="717" alt="Screenshot 2025-03-02 at 10 57 42 AM" src="https://github.com/user-attachments/assets/888fa1a8-6c1a-4b34-9395-e474f59b15ee" />

**Product Segments and Strategies** After applying clustering, products were grouped into three segments based on their sales performance and pricing patterns:

**Segment 0 (Low-Value Product)**

- Low quantity sold, low total sales, and low ASP.
- Struggling in sales or positioned as budget-friendly items.
- Strategy: Improve visibility, offer discounts, and bundle with popular products.

**Segment 1 (Moderate-Value Product)**

- Moderate sales volume, balanced total sales, and mid-range ASP.
- Core products that contribute to steady revenue.
- Strategy: Maintain stock levels, use seasonal promotions, and highlight as "best-value" choices.

**Segment 2 (Best-Selling Product)**

- High quantity sold, high total revenue, and premium ASP.
- High-demand and most profitable products.
- Strategy: Offer exclusive deals, upselling opportunities, and ensure consistent stock availability.

<img width="871" alt="Screenshot 2025-03-02 at 11 03 07 AM" src="https://github.com/user-attachments/assets/1e7f14bd-42e7-4900-b4ac-707002d1bff4" />

## PREDICTIVE CLASSIFICATION MODEL
**Feature Selection:**

- Irrelevant features such as transaction details, product information, and customer IDs were removed to avoid redundancy and improve model focus. The target variable (Segment) was also excluded to prevent data leakage.

**Handling Outliers:**

- Outliers can distort analysis and impact model performance. Winsorization was applied to cap extreme values, reducing their influence while preserving data integrity.

4

**Feature Encoding:**

- Categorical variables like Month and Day of the Week were encoded into numerical values, allowing the model to process them effectively.

**Handling Class Imbalance:**

- Since customer segment is our target, class imbalance was addressed using techniques like oversampling algorithms to prevent bias.

**Train-Test Split:**

- The dataset was split into training (learning patterns) and testing (assessing generalization) sets. This prevents overfitting and ensures robust model   evaluation.

**Model Training:**

- A RandomForestClassifier was trained, leveraging multiple decision trees for improved accuracy and reduced overfitting.

**Predictions & Model Evaluation:**

The model was assessed using a classification report and confusion matrix.

**Confusion Matrix Analysis:**

- Class 0 (Majority Class): 85,097 correct, 256 misclassified as Class 1, 3 as Class 2.

- Class 1: 8,151 correct, 15 misclassified as Class 0.

- Class 2: 11,010 correct, 5 misclassified as Class 0. 🔹Overall, the model performed well, but misclassifications suggest potential improvements through hyperparameter tuning and better feature engineering.

<img width="702" alt="Screenshot 2025-03-02 at 12 20 40 PM" src="https://github.com/user-attachments/assets/a0087e38-6117-4510-83ed-33330d1e7c62" />

## FEATURE IMPORTANCE ANALYSIS

Feature importance reveals which variables most impact the model’s predictions. The RandomForestClassifier ranks features based on their influence using feature_importances_.

**Key Insights:**

- Recency is the top predictor, showing recent purchases strongly influence customer behavior.

- Monetary Value & Frequency are crucial, highlighting spending and shopping habits.

- Month, Quarter & Country have moderate impact on predictions.

- Hour & Days of the Week contribute the least, indicating minimal effect on classification.
<img width="921" alt="Screenshot 2025-03-02 at 12 20 31 PM" src="https://github.com/user-attachments/assets/032797b9-347e-4bb4-b3b0-9a4bdd3829b5" />

**Why It Matters:**

- Identifies key drivers behind model decisions.
- Enables dimensionality reduction, improving efficiency.
- Provides business insights for targeted marketing.
