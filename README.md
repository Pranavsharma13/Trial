**RoadSense: Advanced Predictive Modeling for Traffic Safety**  

The RoadSense project leverages machine learning and deep learning techniques to predict the occurrence and severity of traffic accidents using the US-Accidents dataset, which contains over 2.25 million records. The project employs models like Random Forest, LSTM, CNNs, and Prophet to analyze key factors such as weather, traffic conditions, and time of day. The project utilized Python, Scikit-learn, TensorFlow, and Tableau for data processing, feature engineering, and visualization. With a focus on actionable insights for traffic safety, the application was deployed using Streamlit, providing real-time predictive capabilities. In-depth feature engineering, including dimensionality reduction with PCA and handling class imbalance using SMOTE, resulted in the model achieving 86% accuracy, with a strong emphasis on interpretability to drive better policy and safety decisions.


# 🚦 RoadSense: Advanced Predictive Modeling for Traffic Safety

![RoadSense Banner](https://github.com/user-attachments/assets/roadsense-banner)

## 🏆 Project Overview
**RoadSense** is a machine learning-driven initiative designed to predict and analyze traffic accident severity using the **US-Accidents dataset**, which contains **over 2.25 million records** spanning **2016 to 2023**. The dataset includes **weather conditions, road characteristics, time of day, and accident specifics**, collected from law enforcement reports, traffic cameras, and weather stations.

The project employs **Random Forest, K-Means, DBSCAN, Prophet, and Long Short-Term Memory Networks (LSTM)** to analyze accident trends, severity, and their correlation with environmental and traffic factors. It aims to provide **real-time accident prediction models** for policymakers, urban planners, and traffic safety authorities.

---

## 📌 Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Project Goals & Objectives](#project-goals--objectives)
4. [Dataset Overview](#dataset-overview)
5. [Data Preprocessing & Feature Engineering](#data-preprocessing--feature-engineering)
6. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
7. [Predictive Modeling](#predictive-modeling)
   - [Random Forest Classifier](#random-forest-classifier)
   - [Unsupervised Learning: K-Means & DBSCAN](#unsupervised-learning-k-means--dbscan)
   - [Time Series Forecasting: Prophet](#time-series-forecasting-prophet)
   - [Deep Learning: Long Short-Term Memory (LSTM)](#deep-learning-long-short-term-memory-lstm)
8. [Results & Insights](#results--insights)
9. [Model Interpretability](#model-interpretability)
10. [Conclusion & Future Work](#conclusion--future-work)

---

## 🔹 Introduction
### **Context & Significance**
Traffic accidents pose a significant **socioeconomic burden**, with **over 1.35 million deaths annually** worldwide. Conventional accident prevention measures are often **reactive**, requiring a shift toward **proactive, data-driven approaches**.

---

## 🔹 Problem Statement
The project aims to address the following key questions:
✔ **What factors contribute most to severe traffic accidents?**
✔ **How can real-time weather and traffic data improve accident severity predictions?**
✔ **What are the spatial and temporal patterns of traffic accidents?**
✔ **How can predictive models aid policymakers in designing better road safety measures?**

---

## 🔹 Project Goals & Objectives
### **Key Objectives**
✔ **Develop robust machine learning models** to predict accident severity.
✔ **Identify key risk factors** (weather conditions, traffic signals, time of day, etc.).
✔ **Analyze high-risk accident zones** using clustering techniques.
✔ **Forecast accident trends** for proactive traffic safety interventions.
✔ **Ensure model interpretability** for policymakers and urban planners.

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
   - Imputed missing values for weather and location data.
   - Precipitation, Wind Speed, and Humidity filled with median values.
✔ **Feature Engineering**:
   - Extracted **Start_Hour, Start_Minute, Start_Second** from Start_Time.
   - **Encoded categorical variables** (e.g., Weather_Condition) using Label Encoding.
✔ **Dimensionality Reduction**:
   - **Principal Component Analysis (PCA)** retained six principal components.
✔ **Class Imbalance Handling**:
   - Applied **SMOTE** (Synthetic Minority Oversampling) to balance severity classes.
✔ **Dataset Splitting:** 80-20 train-test split.

---

## 🔹 Results & Insights
### **4.1 Results Overview**
This section summarizes the performance of the various machine learning models developed to predict traffic accident severity, cluster accident patterns, and forecast daily severity based on historical data.

### **4.2 Model Performance**
| Model | Type | Metrics | Strengths | Weaknesses |
|--------|---------|-------------------------|--------------------------------------------------|--------------------------------------------------|
| **Random Forest** | Classification | - Accuracy: **86%**  | - Strong performance for **Classes 1 and 4** | - Difficulty distinguishing between **Classes 2 and 3** |
|  |  | - Precision: Highest for **Class 1 and 4 (91%)** | - High recall for **Class 1 (99%)** | - Overlapping feature patterns affecting prediction accuracy |
| **K-Means Clustering** | Clustering | - Silhouette Score: **0.65** | - Well-defined and **separated clusters** | - Sensitive to **initial centroid selection** |
| **DBSCAN Clustering** | Clustering | - No fixed metric due to algorithm nature | - Identifies clusters with **varying densities** | - Performance depends on **eps and min_samples** |
| **Prophet** | Time Series Forecasting | - Accuracy: Strong **alignment of actual vs. predicted** | - Captures **temporal patterns and trends** | - Depends on **data quality and availability** |
| **LSTM** | Time Series Analysis | - **MAE: 0.31** | - Accurate predictions of **traffic patterns** | - Requires **significant data preprocessing** |

---

## 🔹 Conclusion & Future Work
🚀 **Next Steps for RoadSense**:
✅ **Further Feature Engineering** to improve accuracy for **Classes 2 & 3**.
✅ **Integration of Real-Time Data** for **dynamic predictions**.
✅ **Deploy a Live Dashboard** for **real-time accident risk assessment**.
✅ **Collaborate with authorities** to implement **data-driven safety policies**.

---

## 📌 Get in Touch
📧 pranavsharma1395@gmail.com  
📞 +1 (778) 598-6373  
🌐 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  
🔗 **Project Repository**: [GitHub Link](https://github.com/user/RoadSense)

📢 *"Leveraging AI to Make Roads Safer!"* 🚗💨
