# Customer Portrait Analysis - [Nam Bắc Consulting]

This repository contains the analysis and insights from our customer segmentation project for the DAZONE 2024 Data Analysis Competition, powered by Viettel. The goal of this analysis is to understand customer behaviors, segment customers into actionable groups, and optimize marketing strategies to drive revenue.

## Project Overview

In this project, we:
1. **Preprocessed Data**: Handled duplicates and missing values to ensure data integrity, resulting in a dataset with **25,000 unique customer records**.
2. **Segmentation**: Conducted customer segmentation using demographic and transactional data across **10 key variables**.
3. **Promotion Analysis**: Assessed customer response to **5 different promotions** to identify and target high-value segments.
4. **Customer Journey Mapping**: Identified **4 main customer touchpoints** and formulated hypotheses to improve conversion rates.


## Feature Selection

In this project, feature selection played a critical role in identifying the most relevant variables for customer segmentation and predictive analysis. By carefully selecting features, we improved model accuracy, reduced processing time, and ensured that the insights were actionable for optimizing marketing strategies.

### Feature Selection Process
![image](https://github.com/user-attachments/assets/1bfbd6c4-c5fe-4925-89fc-d18c4188bd54)

1. **Correlation Analysis**:
   - Conducted correlation analysis to identify highly correlated variables that could introduce redundancy. For example, high correlations between certain demographic features like **Age** and **Income** led us to select only the most informative ones for segmentation.
   - **Pearson correlation coefficient** was used for continuous variables, while **Cramér's V** was employed for categorical variables.

2. **Univariate and Bivariate Analysis**:
   - **Univariate Analysis**: Helped in understanding the distribution of each variable. We prioritized variables that showed significant variability among customers, such as **total purchase value** and **frequency of store visits**.
   - **Bivariate Analysis**: Analyzed relationships between potential features and the target variable (customer segments). Features like **purchase frequency** and **average spending per visit** were selected due to their strong association with customer engagement levels.

3. **Principal Component Analysis (PCA)**:
   - **PCA** was used to reduce dimensionality and retain features with the highest variance, especially where multicollinearity was present. This allowed us to capture the most significant aspects of customer behavior without losing critical information.

4. **Domain Knowledge**:
   - Leveraged business expertise to prioritize industry-relevant features, such as **preferred purchase channel** (online vs. in-store) and **response to promotions** based on known customer behavior patterns.

### Selected Features

After conducting the feature selection process, the following features were identified as the most impactful for our analysis:
![image](https://github.com/user-attachments/assets/dad30bc7-8b44-4900-ba68-23cc88940820)

- **Demographics**:
  - **Age**: Older customers exhibited different purchasing patterns compared to younger segments.
  - **Income**: A key indicator that influenced average transaction value and customer loyalty.

- **Behavioral Attributes**:
  - **Purchase Frequency**: Differentiated one-time buyers from repeat customers.
  - **Average Transaction Value**: Essential for identifying high-value customers who contribute significantly to revenue.
  - **Purchase Recency**: Helped identify inactive or at-risk customers who may need targeted re-engagement.

- **Product Preferences**:
  - **Top Product Categories**: Insights into category-driven behavior allowed for more personalized marketing approaches.
  - **Category Spend Ratio**: The distribution of spending across different categories helped to identify customers with niche interests or broad buying patterns.

## Key Findings


![image](https://github.com/user-attachments/assets/40e56192-fd32-43f5-b9b9-9c9a2bff5fd0)

- **Revenue Breakdown**: **Liquor** and **Pork** categories make up **80% of total revenue**.

![image](https://github.com/user-attachments/assets/604d80e7-41f4-4a04-ade0-eaba1f57ece1)
- **Customer Insights**:
  - **65%** of customers prefer in-store purchases.
  - Repeat customers typically revisit after **49 days**, averaging **14 orders** and generating approximately **$608** in annual revenue.
- **Segment Analysis**:
  - **Six customer segments** were identified using K-means clustering, including **Loyal Customers**, **Champions**, and **Need Attention** groups.
  - The "Need Attention" group, comprising **66% of customers**, contributes **49% of revenue** but has low engagement, presenting an opportunity for targeted retention strategies.
![image](https://github.com/user-attachments/assets/4280a45c-fc9f-4398-b187-13edc793c2e4)

## Methodology
1. **Data Cleaning**: Removed duplicates, handled missing values with linear regression for income estimation, and merged phone data, resulting in a **cleaned dataset** of **1 million transactions**.
2. **Segmentation**: Used **K-means clustering** to divide customers into six segments based on their purchasing behavior, demographics, and interaction history.
3. **Promotion Effectiveness**: Evaluated acceptance rates across five promotions, revealing that **Promotion B** had the highest engagement among loyal customers, while **Promotion C** drove initial interest from new customers.


