**RoadSense: Advanced Predictive Modeling for Traffic Safety**  

The RoadSense project leverages machine learning and deep learning techniques to predict the occurrence and severity of traffic accidents using the US-Accidents dataset, which contains over 2.25 million records. The project employs models like Random Forest, LSTM, CNNs, and Prophet to analyze key factors such as weather, traffic conditions, and time of day. The project utilized Python, Scikit-learn, TensorFlow, and Tableau for data processing, feature engineering, and visualization. With a focus on actionable insights for traffic safety, the application was deployed using Streamlit, providing real-time predictive capabilities. In-depth feature engineering, including dimensionality reduction with PCA and handling class imbalance using SMOTE, resulted in the model achieving 86% accuracy, with a strong emphasis on interpretability to drive better policy and safety decisions.


# 🚦 RoadSense: Advanced Predictive Modeling for Traffic Safety
Access the RoadSense App here: https://roadsense-trafficsaftey.streamlit.app/
![Screenshot 2025-02-13 at 8 10 36 PM](https://github.com/user-attachments/assets/76121b2f-6d29-45a8-bb9d-0b6be029584c)

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

## 🔹 Results & Insights
### **4.1 Results Overview**
This section summarizes the performance of the various machine learning models developed to predict traffic accident severity, cluster accident patterns, and forecast daily severity based on historical data.

### **4.2 Model Performance**
| Model | Type | Metrics | Strengths | Weaknesses |
|--------|---------|-------------------------|--------------------------------------------------|--------------------------------------------------|
| **Random Forest** | Classification | - Accuracy: **86%**  | - Strong performance for **Classes 1 and 4** | - Difficulty distinguishing between **Classes 2 and 3** |
|  |  | - Precision: Highest for **Class 1 and 4 (91%)** | - High recall for **Class 1 (99%)** | - Overlapping feature patterns affecting prediction accuracy |
|  |  | - F1-Score: High for **Class 1 and 4** | - Performs well in predicting **low and high severity accidents** |  |
| **K-Means Clustering** | Clustering | - Silhouette Score: **0.65** | - Well-defined and **separated clusters** | - Sensitive to **initial centroid selection** |
|  |  |  | - Effective in identifying general clusters | - Struggles with **non-globular clusters** |
| **DBSCAN Clustering** | Clustering | - No fixed metric due to algorithm nature | - Identifies clusters with **varying densities** | - Performance depends on **eps and min_samples** |
|  |  |  | - Captures **outliers and core points** effectively |  |
| **Prophet** | Time Series Forecasting | - Accuracy: Strong **alignment of actual vs. predicted** | - Captures **temporal patterns and trends** | - Depends on **data quality and availability** |
|  |  |  | - Provides insights into **seasonal patterns** | - Choice of **regressors impacts accuracy** |
| **LSTM** | Time Series Analysis | - **MAE: 0.31** | - Accurate predictions of **traffic patterns** | - Requires **significant data preprocessing** |
|  |  | - Loss: **Decreased over 100 epochs** | - Effective in **learning complex temporal dependencies** | - Sensitive to **hyperparameters and model architecture** |

📌 **Key Takeaways:**
- **Random Forest performed best for classification**, accurately predicting accident severity with **86% accuracy**.
- **K-Means successfully identified general accident zones**, but struggled with **non-globular clusters**.
- **DBSCAN effectively detected accident hotspots**, particularly in **dense urban areas**.
- **Prophet forecasted seasonal accident patterns**, aiding in long-term **traffic safety planning**.
- **LSTM demonstrated strong predictive capabilities**, particularly in understanding **traffic flow trends** over time.

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
