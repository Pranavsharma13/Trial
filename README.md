# 📊 FundWise: Deciphering Mutual Fund Performance & Behavior

![FundWise Banner](https://github.com/user-attachments/assets/b96c2538-8181-4ebe-bb91-740b7e27eb9a)

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

---

## 🔹 Introduction
Mutual fund investment decisions require data-driven insights. This project seeks to understand how fund characteristics influence performance, providing actionable recommendations for investors.

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

---

## 🔹 Data Cleaning & Preprocessing
✔ **Missing Data Handling**: Mean/zero-fill techniques applied to key columns.  
✔ **Outlier Treatment**: Statistical detection & removal.  
✔ **Feature Engineering**: Created a ‘Total Investment’ column for comprehensive portfolio analysis.

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

---

## 🔹 Visualization & Findings
📊 **Commencement & Maturity Trends**: 2015 had the highest fund maturity count.  
📊 **Expense Ratio vs. Returns**: Negative correlation—lower expenses often yield better performance.  
📊 **Fund Size & Investment Type**: Growth funds show a direct relationship with size in return rates.  

---

## 🔹 Predictive Modeling
🧠 **Machine Learning Models Used**:
- **Extra Tree Regressor**: Best predictive model with R² = 96.17%
- **Random Forest**: R² = 95.09%
- **Decision Tree**: R² = 87.94%

📌 **Model Insights**:
- **Higher fund ratings correlate with better return predictions.**
- **Expense ratio plays a crucial role in fund sustainability.**

---

## 🔹 Fund Classification
🏆 **Top 5 Performing Funds**
1. **AGEIX** – Highest Return Ratio (0.05810%)
2. **Cohen & Steers Funds** – Strong performers in small-sized funds.

🚨 **Bottom 5 Performing Funds**
1. **FFRLX** – Virtus Family underperformed.
2. **FRICX** – William Blair held the lowest position.

✅ **Safe Investment Funds**
- **ETAHX (Small-sized)** – Best in 3, 5, and 10-year performance.
- **GHYMX & ETCTX** – Stable historical returns.

---

## 🔹 Conclusion & Strategic Insights
📌 **Key Takeaways**:
- **Diversification is essential**: Small-sized funds perform well in Financial Services, while large funds thrive in Tech.
- **Fund Ratings & ROI Correlation**: Ratings act as a strong indicator of performance.
- **Expense Ratio Matters**: Funds with lower expense ratios tend to yield better returns.

---

## 🔹 Future Work
✅ **Advanced Deep Learning**: Neural networks for fund return forecasting.  
✅ **Portfolio Optimization Strategies**: AI-based allocation tools.  
✅ **Interactive Dashboards**: Dynamic Tableau/Power BI visualizations.  
✅ **Market Sentiment Analysis**: Using NLP to predict fund trends.

---

## 📌 Get in Touch
📧 pranavsharma1395@gmail.com  
📞 +1 (778) 598-6373  
🌐 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  

🔗 **Project Repository**: [GitHub Link](https://github.com/user/FundWise)

---
📢 *"Empowering Investors with Data-Driven Insights!"*
