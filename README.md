**RoadSense: Advanced Predictive Modeling for Traffic Safety**  

The RoadSense project leverages machine learning and deep learning techniques to predict the occurrence and severity of traffic accidents using the US-Accidents dataset, which contains over 2.25 million records. The project employs models like Random Forest, LSTM, CNNs, and Prophet to analyze key factors such as weather, traffic conditions, and time of day. The project utilized Python, Scikit-learn, TensorFlow, and Tableau for data processing, feature engineering, and visualization. With a focus on actionable insights for traffic safety, the application was deployed using Streamlit, providing real-time predictive capabilities. In-depth feature engineering, including dimensionality reduction with PCA and handling class imbalance using SMOTE, resulted in the model achieving 86% accuracy, with a strong emphasis on interpretability to drive better policy and safety decisions.


# 🚦 RoadSense: Advanced Predictive Modeling for Traffic Safety
Access the RoadSense App here: https://roadsense-trafficsaftey.streamlit.app/
![Screenshot 2025-02-13 at 8 10 36 PM](https://github.com/user-attachments/assets/76121b2f-6d29-45a8-bb9d-0b6be029584c)

# 🚦 RoadSense: Advanced Predictive Modeling for Traffic Safety

![RoadSense Banner](https://github.com/user-attachments/assets/roadsense-banner)

## 🏆 Project Overview
**RoadSense** is a machine learning-driven initiative designed to predict and analyze traffic accident severity using the **US-Accidents dataset**, which contains **over 2.25 million records** spanning **2016 to 2023**. The dataset includes **weather conditions, road characteristics, time of day, and accident specifics**, collected from law enforcement reports, traffic cameras, and weather stations.

The project employs **Random Forest, Gradient Boosting Machines (GBM), Deep Neural Networks (DNNs), Convolutional Neural Networks (CNNs), and Long Short-Term Memory Networks (LSTM)** to analyze accident trends, severity, and their correlation with environmental and traffic factors. It aims to provide **real-time accident prediction models** for policymakers, urban planners, and traffic safety authorities.

---

## 📌 Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Project Goals & Objectives](#project-goals--objectives)
4. [Dataset Overview](#dataset-overview)
5. [Data Preprocessing & Feature Engineering](#data-preprocessing--feature-engineering)
6. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
7. [Predictive Modeling](#predictive-modeling)
8. [Results & Insights](#results--insights)
9. [Model Interpretability](#model-interpretability)
10. [Conclusion & Future Work](#conclusion--future-work)

---

## 🔹 Introduction
### **Context & Significance**
Traffic accidents are a critical global issue, causing over **1.35 million deaths annually** and leading to major economic and societal burdens. The increasing complexity of urban traffic systems necessitates **data-driven safety measures**. Predictive modeling enables **proactive risk mitigation** by identifying accident-prone conditions before they occur.

---

## 🔹 Problem Statement
The project aims to address the following key questions:
✔ **What are the most significant factors contributing to severe traffic accidents?**
✔ **How can real-time weather and traffic data enhance accident severity predictions?**
✔ **What are the spatiotemporal patterns of accidents, and how can they inform safety policies?**

---

## 🔹 Project Goals & Objectives
### **Key Objectives**
✔ **Develop accurate machine learning models** to predict accident severity.
✔ **Identify key risk factors** (weather conditions, traffic signals, time of day, etc.).
✔ **Analyze high-risk accident zones** using clustering techniques.
✔ **Forecast accident trends** for proactive traffic safety interventions.
✔ **Ensure model interpretability** for policymakers.

---

## 🔹 Dataset Overview
📂 **Dataset**: US-Accidents (2016 - 2023) ([Kaggle](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents))  
📊 **Size**: 2.25 million records | 46 features  
🌍 **Geographical Coverage**: Entire contiguous US states  

### **Key Features**
- **Severity**: 1 (least severe) to 4 (most severe)
- **Weather Conditions**: Rain, Snow, Fog, Temperature, Wind Speed, Visibility
- **Traffic Infrastructure**: Traffic Signals, Stop Signs, Crosswalks
- **Location & Time**: Date, Time of Day, City, State, Road Type

---

## 🔹 Data Preprocessing & Feature Engineering
✔ **Handling Missing Values**:
   - Imputation applied for missing weather and location data.
   - Precipitation, Wind Speed, and Humidity filled with median values.
✔ **Feature Engineering**:
   - Created **‘Accident Hotspot Score’** based on accident frequency.
   - Derived **‘Time of Day Segmentation’** (Morning, Afternoon, Evening, Night).
✔ **Class Imbalance Handling**:
   - **SMOTE (Synthetic Minority Over-sampling Technique)** used to balance severity classes.
✔ **Dimensionality Reduction**:
   - **Principal Component Analysis (PCA)** applied to optimize feature selection.

---

## 🔹 Exploratory Data Analysis (EDA)
📌 **Key Insights**:
- **Highest Accident Frequency**: **California (22,702 cases)**
- **Most Accidents in a City**: **Miami (2,410 cases in CA)**
- **Peak Accident Hours**: **7-9 AM & 4-6 PM**
- **High Risk Factors**:
  - **Low visibility and heavy precipitation significantly increase accident severity.**
  - **Urban intersections experience frequent but lower severity accidents.**
  - **High-speed highways tend to have fewer but more severe accidents.**

---

## 🔹 Predictive Modeling
🧠 **Machine Learning Models Used**:

### **Accident Severity Classification Models**
- **Random Forest** (Best Performing - **86% Accuracy**)
- **Gradient Boosting Machines (GBM)**
- **Deep Neural Networks (DNNs)**
- **Convolutional Neural Networks (CNNs)**
- **Long Short-Term Memory Networks (LSTM)**

### **High-Risk Zone Clustering Models**
- **K-Means**
- **DBSCAN (Density-Based Clustering)**

### **Time Series Forecasting for Accident Trends**
- **Prophet** (Daily severity forecasting by location)

📌 **Performance Highlights**:
- **Random Forest achieved the best classification performance**:
  - **F1-Score: 0.91, ROC-AUC: 0.95**
  - **Most influential factors**: Weather Conditions, Visibility, Time of Day
- **K-Means & DBSCAN identified high-risk zones**:
  - **Clusters of high accident severity in major intersections and highways.**

---

## 🔹 Results & Insights
🏆 **Final Model Performance Summary**
| Model | Accuracy | F1-Score | ROC-AUC |
|--------|---------|---------|---------|
| **Random Forest** | **86%** | **0.91** | **0.95** |
| Gradient Boosting | 83% | 0.88 | 0.91 |
| DNN | 81% | 0.85 | 0.88 |

📌 **Key Takeaways**:
- **Weather and traffic conditions have a direct correlation with accident severity.**
- **Machine learning models effectively predict severity and detect high-risk zones.**
- **Prophet's time-series forecasting provides real-time accident trend analysis.**

---

## 🔹 Model Interpretability
📌 **Feature Importance Analysis**
- **Top Contributing Factors to Severity Predictions**:
  - **Weather Conditions** (Rain, Snow, Fog, Low Visibility)
  - **Time of Day** (Rush Hours show more severe accidents)
  - **Road Type** (Highways have the highest severity levels)

📌 **SHAP & LIME for Explainability**
- SHAP values highlight how **individual factors contribute to accident severity.**
- LIME explains **how the models make predictions for specific cases.**

---

## 🔹 Conclusion & Future Work
🚀 **Next Steps for RoadSense**:
✅ **Integrate real-time traffic & weather data** for dynamic risk analysis.
✅ **Enhance deep learning models (CNNs, Autoencoders) for improved predictions.**
✅ **Develop an interactive dashboard for policymakers.**

---

## 📌 Get in Touch
📧 pranavsharma1395@gmail.com  
📞 +1 (778) 598-6373  
🌐 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  
🔗 **Project Repository**: [GitHub Link](https://github.com/user/RoadSense)

📢 *"Leveraging AI to Make Roads Safer!"* 🚗💨
