# 📊 FundWise: Deciphering Mutual Fund Performance & Behavior

![FundWise Banner]![Fundwiser Presentation_page-0001](https://github.com/user-attachments/assets/3b309a03-9c12-4fa2-88f3-375fce0ff835)


## 🏆 Project Overview
FundWise is a comprehensive data analysis and machine learning project focused on evaluating mutual fund performance, exploring portfolio compositions, risk-return profiles, expense ratios, and predictive modeling to guide investment strategies. The project includes rigorous data cleaning, visualization, and predictive modeling for actionable insights.

## 📌 Table of Contents
1. [Executive Summary](#executive-summary)
2. [Introduction](#introduction)
3. [Data Overview](#data-overview)
4. [Data Cleaning & Preprocessing](#data-cleaning--preprocessing)
5. [Exploratory Data Analysis](#exploratory-data-analysis)
6. [Visualization & Findings](#visualization--findings)
7. [Predictive Modeling](#predictive-modeling)
8. [Fund Classification](#fund-classification)
9. [Conclusion & Strategic Insights](#conclusion--strategic-insights)
10. [Future Work](#future-work)

---

## 🔹 Executive Summary
### **Objective**
The objective of this analysis is to decode mutual fund behavior, focusing on:
- Portfolio composition & sectoral allocation
- Risk-return profiles and expense ratios
- Fund maturity trends and investor confidence
![Fundwiser Presentation_page-0005](https://github.com/user-attachments/assets/979caea8-2ad3-4c1e-93c8-f7f821ae915e)

### **Key Insights & Outcomes**
📌 **Initial Investment Trends**: Investments range from $10 to $5B, with common entry points at $1,000, $2,500, and $1M.
📌 **Maturity Trends**: 2015 saw the highest number of fund maturities (505), and average yields fluctuated from 0.03% (1968) to 22.35% (2015).
📌 **ROI & Volatility**: High fluctuations in earlier years (e.g., 25.27% in 1974), but stabilizing in recent years.
📌 **Morningstar Ratings**: Peaked in 1975 (4.50/5), bottomed in 2020 (1.099/5).
📌 **Sectoral Allocation**: Financial services consistently dominate, with small funds focusing on financials, mid-sized funds in real estate, and large funds in technology.
📌 **Fund Performance**:
   - **Top Performer**: AGEIX (Return Ratio: 0.05810%)
   - **Bottom Performer**: CPXAX (Virtus Family)
   - **Safe Zone Funds**: ETAHX, GHYMX, ETCTX leading in 3, 5, and 10-year performance.
📌 **Machine Learning Models**: Extra Tree Regressor outperformed other models (R² = 96.17%) in predicting fund returns.
![Fundwiser Presentation_page-0002](https://github.com/user-attachments/assets/dba15331-5081-4d35-8c98-f57ffbba10a1)

---

## 🔹 Introduction
Mutual fund investment decisions require data-driven insights. This project seeks to understand how fund characteristics influence performance, providing actionable recommendations for investors.
![Fundwiser Presentation_page-0003](https://github.com/user-attachments/assets/9f99a6c0-4e34-43e4-a225-7c6e41c0cf6d)

### **Key Business Questions**
- How does portfolio composition impact sector exposure and risk?
- What are the historical patterns in fund maturity and performance?
- Can machine learning models improve fund return predictions?

### **Stakeholders**
- **Investment Committees & Fund Managers**: Data-backed decisions for fund allocation.
- **Individual & Institutional Investors**: Strategic investment insights.
- **Data Analysts & Scientists**: Research on financial market trends.

---

## 🔹 Data Overview
📂 **Dataset**: MutualFunds.csv ([Kaggle](https://www.kaggle.com/datasets/stefanoleone992/mutual-funds-and-etfs))  
📊 **Size**: 23,784 rows | 298 columns  
💡 **Key Features**: Net assets, expense ratio, turnover, risk ratings, growth metrics, historical returns.
![Fundwiser Presentation_page-0004](https://github.com/user-attachments/assets/d897b6e3-5eea-4fb2-b69a-a13364287bd5)

---

## 🔹 Data Cleaning & Preprocessing
✔ **Missing Data Handling**: Mean/zero-fill techniques applied to key columns.  
✔ **Outlier Treatment**: Statistical detection & removal.  
✔ **Feature Engineering**: Created a ‘Total Investment’ column for comprehensive portfolio analysis.
![Fundwiser Presentation_page-0006](https://github.com/user-attachments/assets/eab3d9de-b7af-4909-9b6d-309d5ed6a585)

---

## 🔹 Exploratory Data Analysis (EDA)
📌 **Univariate, Bivariate & Multivariate Analysis**
📊 **Key Findings**:
- **ROI Trends**: Early years had high volatility; recent years show stabilization.
- **Morningstar Ratings**: Fluctuated significantly, peaking in 1975 and dropping in 2020.
- **Sectoral Allocation by Fund Size**:
  - **Small Funds**: Highest in Financial Services.
  - **Mid-Size Funds**: Dominated by Real Estate.
  - **Large Funds**: Focus on Technology.
![Fundwiser Presentation_page-0007](https://github.com/user-attachments/assets/efae4240-01ca-4128-b1bd-99b585a1bae8)

---

## 🔹 Visualization & Findings
📊 **Commencement & Maturity Trends**: 2015 had the highest fund maturity count.  
📊 **Expense Ratio vs. Returns**: Negative correlation—lower expenses often yield better performance.  
📊 **Fund Size & Investment Type**: Growth funds show a direct relationship with size in return rates.  
![Fundwiser Presentation_page-0008](https://github.com/user-attachments/assets/33d937c3-1eae-4ef5-a147-58c949723448)
![Fundwiser Presentation_page-0009](https://github.com/user-attachments/assets/c63d142a-b9d3-4760-bc62-13f05fb66239)
![Fundwiser Presentation_page-0010](https://github.com/user-attachments/assets/482a82f4-0749-4ffe-8821-196325adbe95)
![Fundwiser Presentation_page-0011](https://github.com/user-attachments/assets/cf8c486b-3263-4569-bec7-dd69757b76f8)
![Fundwiser Presentation_page-0012](https://github.com/user-attachments/assets/d205cabc-9430-48fa-93fe-78e6b4486b72)
![Fundwiser Presentation_page-0013](https://github.com/user-attachments/assets/374fa625-fe18-447b-bf3a-fe35dd1c7b68)
![Fundwiser Presentation_page-0014](https://github.com/user-attachments/assets/d3fc0688-c973-4e67-9f36-2dab0fe64004)
![Fundwiser Presentation_page-0020](https://github.com/user-attachments/assets/0895592e-d84f-4e7b-9fab-4bb32d0a27d8)

---

## 🔹 Predictive Modeling
🧠 **Machine Learning Models Used**:
- **Extra Tree Regressor**: Best predictive model with R² = 96.17%
- **Random Forest**: R² = 95.09%
- **Decision Tree**: R² = 87.94%

📌 **Model Insights**:
- **Higher fund ratings correlate with better return predictions.**
- **Expense ratio plays a crucial role in fund sustainability.**
![Fundwiser Presentation_page-0016](https://github.com/user-attachments/assets/3f319964-3293-4010-ab14-2f27767fdc2a)

---

## 🔹 Fund Classification
🏆 **Top 5 Performing Funds**
1. **AGEIX** – Highest Return Ratio (0.05810%)
2. **Cohen & Steers Funds** – Strong performers in small-sized funds.
![Fundwiser Presentation_page-0017](https://github.com/user-attachments/assets/8dec4b22-6f6e-4ed7-8a98-dd0bdd4c1301)

🚨 **Bottom 5 Performing Funds**
1. **FFRLX** – Virtus Family underperformed.
2. **FRICX** – William Blair held the lowest position.
![Fundwiser Presentation_page-0018](https://github.com/user-attachments/assets/96d7cbcf-0af1-4d91-9937-1eec9cb9a2e5)

✅ **Safe Investment Funds**
- **ETAHX (Small-sized)** – Best in 3, 5, and 10-year performance.
- **GHYMX & ETCTX** – Stable historical returns.
![Fundwiser Presentation_page-0019](https://github.com/user-attachments/assets/e7be58db-7b98-4bbb-9891-3b45ca951376)

---

## 🔹 Conclusion & Strategic Insights
📌 **Key Takeaways**:
- **Diversification is essential**: Small-sized funds perform well in Financial Services, while large funds thrive in Tech.
- **Fund Ratings & ROI Correlation**: Ratings act as a strong indicator of performance.
- **Expense Ratio Matters**: Funds with lower expense ratios tend to yield better returns.
![Fundwiser Presentation_page-0022](https://github.com/user-attachments/assets/6caeae3d-af52-4ef7-b416-2f6e58c9789a)
![Fundwiser Presentation_page-0021](https://github.com/user-attachments/assets/44cbaa62-884b-4785-82d4-fce24b27d713)

---

## 🔹 Future Work
✅ **Advanced Deep Learning**: Neural networks for fund return forecasting.  
✅ **Interactive Dashboards**: Dynamic Tableau/Power BI visualizations.  
✅ **Market Sentiment Analysis**: Using NLP to predict fund trends.

---

## 📌 Get in Touch
📧 pranavsharma1395@gmail.com  
🌐 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  

🔗 **Project Repository**: [GitHub Link](https://github.com/user/FundWise)

---
📢 *"Empowering Investors with Data-Driven Insights!"*
