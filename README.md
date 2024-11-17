# **Medical Inventory Optimization**

This project focuses on analyzing and optimizing medical inventory data for healthcare facilities. It identifies inefficiencies in inventory management, such as high return rates and seasonal demand fluctuations, and provides actionable recommendations to reduce waste, improve stock levels, and optimize costs.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Dataset Details](#dataset-details)
- [Approach and Analysis](#approach-and-analysis)
- [Key Findings](#key-findings)
  - [High Return Categories](#high-return-categories)
  - [Seasonal Trends](#seasonal-trends)
  - [Department-Level Analysis](#department-level-analysis)
  - [Bounce Rate](#bounce-rate)
- [Technologies Used](#technologies-used)
- [Conclusion](#conclusion)

---

## **Introduction**

Inventory management is critical in healthcare to avoid overstocking, understocking, or wastage of medical supplies. This project uses historical data analysis and visualization to:
- Identify patterns in sales and returns.
- Optimize inventory for high-demand seasons.
- Minimize return rates by understanding inefficiencies.

---

## **Problem Statement**

Healthcare providers face several inventory challenges:
1. **Overstocking**: Excess inventory leads to higher storage costs and product expiration.  
2. **Understocking**: Insufficient inventory risks patient care.  
3. **High Return Rates**: Returns increase wastage and reflect inaccurate demand forecasting.  
4. **Seasonal Demand**: Lack of preparation for demand spikes during peak seasons leads to operational inefficiencies.

This project analyzes historical sales and return data to address these problems.

---

## **Dataset Details**

- **Size**: 14,218 rows and 14 columns  
- **Attributes**:
  - `Typeofsales`: Indicates whether the transaction was a sale or return.
  - `Quantity` and `ReturnQuantity`: Quantities sold and returned.
  - `Final_Sales`: Revenue generated per transaction.
  - `Formulation`: Drug type (e.g., Injections, Tablets).
  - `SubCat`: Product subcategory.
  - `Dateofbill`: Date of each transaction (used to derive seasonal trends).
- **Challenges**:
  - Missing values in key categorical columns like `Formulation` and `DrugName`.
  - Duplicate rows in the dataset.
  - Identifying meaningful insights from large datasets.

---

## **Approach and Analysis**

1. **Data Cleaning**:
   - Handled missing values in categorical columns using mode imputation.
   - Removed 26 duplicate rows to ensure dataset integrity.

2. **Feature Engineering**:
   - Created a `BounceRate` metric: percentage of returned items relative to sold quantities.
   - Extracted seasonal patterns using the `Dateofbill` column.

3. **Exploratory Data Analysis (EDA)**:
   - Visualized trends in sales and returns by categories, departments, and time periods.
   - Highlighted seasonal and department-specific inefficiencies.

4. **Insights Extraction**:
   - Grouped data by categories (`SubCat`, `Formulation`) and departments to uncover trends.
   - Identified high-return categories and months with peak sales.

---

## **Key Findings**

### **1. High Return Categories**
- **Injections**: The most returned category, with 926 returns.
- **IV Fluids and Electrolytes**: Significant returns (475) due to overstocking or quality issues.
- **Tablets & Capsules**: Moderate return rates (94 returns).
- **Recommendation**:  
  - Adjust procurement for these categories to align with demand patterns.
  - Investigate reasons for high returns in Injections and IV Fluids.

---

### **2. Seasonal Trends**
- Sales peaked during **April**, **August**, and **December**, termed as **High Seasons**.  
- Lower demand observed in **January**, **June**, and **September** (**Low Seasons**).  
- **Revenue Insights**:
  - **High Season Average Revenue**: ₹248 per transaction.
  - **Low Season Average Revenue**: ₹226 per transaction.
- **Recommendation**:
  - Increase stock levels for high-demand products during peak seasons.
  - Optimize inventory by reducing quantities during low seasons.

---

### **3. Department-Level Analysis**
- **Department 1** had the highest number of returns, with **Specialization 4** leading the returns.  
- **Recommendation**:
  - Investigate operational inefficiencies in Department 1.
  - Train staff to minimize errors in handling and ordering inventory.

---

### **4. Bounce Rate**
- **Definition**: The percentage of items returned relative to sold quantities.  
- **Observation**: Average bounce rate is very low (near 0%), indicating efficient inventory handling.  
- **Recommendation**:
  - Maintain current practices but focus on high-return items to further reduce waste.

---

## **Technologies Used**

- **Languages and Libraries**:
  - Python: Pandas, NumPy, Matplotlib, Seaborn, Plotly.
- **Tools**:
  - Google Colab for analysis and visualization.
- **Techniques**:
  - Data cleaning, feature engineering, EDA, and visualization.

---
## **Conclusion**

This project demonstrates my ability to apply data analysis and optimization techniques to solve real-world challenges in healthcare inventory management. By leveraging advanced data preprocessing, feature engineering, and exploratory data analysis (EDA), I successfully identified patterns and inefficiencies that can significantly improve inventory practices.

Key outcomes of the project include:
- **Optimized Inventory**: Recommendations that can reduce overstocking and understocking, directly impacting cost reduction and operational efficiency.
- **Improved Demand Forecasting**: Insights into seasonal trends and product returns that allow healthcare facilities to better plan for peak demand periods.
- **Actionable Insights**: Identified high-return product categories and areas for inventory adjustments, leading to a more efficient and cost-effective supply chain.

This project highlights my proficiency in data analysis, problem-solving, and the ability to generate actionable business insights. Moving forward, further enhancements such as machine learning models and real-time data integration can make this solution even more robust, providing even greater value to healthcare organizations.


