# 🚀 ShopperLens: AI-Driven Personalized Recommendation System

![ShopperLens Banner](https://github.com/user-attachments/assets/shopperlens-banner)

## 📌 Project Overview
ShopperLens is a **multi-model recommendation system** designed to predict and personalize product recommendations for e-commerce users based on **session data, user interactions, and product attributes**. This project implements **three distinct recommendation approaches** to optimize relevance and engagement.

### 🔥 **Key Features**
✅ **Memory-Based Model (LightGBM)** – Analyzes session-based data for color prediction.  
✅ **Collaborative Filtering (SVD + LightGBM)** – Learns hidden patterns from user-item interactions.  
✅ **Item-Based Filtering (KNN)** – Recommends similar products using cosine similarity.

### 🏗 **System Architecture**
ShopperLens follows a **multi-branch architecture** with independent pipelines for each recommendation strategy:

![System Architecture](https://github.com/user-attachments/assets/shopperlens-architecture)

---

## 📌 Table of Contents
1. [🔍 Problem Statement](#-problem-statement)
2. [📊 Dataset Details](#-dataset-details)
3. [🛠 Data Preprocessing](#-data-preprocessing)
4. [🧠 Recommendation Models](#-recommendation-models)
   - [Branch 1: Memory-Based Model (LightGBM)](#branch-1-memory-based-model-lightgbm)
   - [Branch 2: Collaborative Filtering (SVD + LightGBM)](#branch-2-collaborative-filtering-svd--lightgbm)
   - [Branch 3: Item-Based Filtering (KNN)](#branch-3-item-based-filtering-knn)
5. [📌 Results & Insights](#-results--insights)
6. [🚀 Future Enhancements](#-future-enhancements)
7. [📚 References](#-references)

---

## **🔍 Problem Statement**
E-commerce platforms face challenges in delivering **highly relevant recommendations** due to:
- **Sparse user-item interaction data** affecting prediction accuracy.
- **Cold start problem** for new users and products.
- **Balancing personalization vs. diversity** in suggestions.

ShopperLens tackles these issues using a **multi-approach recommendation system** to improve recommendation accuracy and enhance user engagement.

---

## **📊 Dataset Details**
The dataset used for this project is **E-Shop Clothing 2008**, containing:
- **User Sessions** – Tracks clicks, views, and purchase interactions.
- **Product Details** – Includes attributes like color, category, price, metadata.
- **Transaction Data** – Captures orders, session IDs, and timestamps.

🔹 **Preprocessing Steps:**
✅ Handling **missing values** using mean/mode imputation.  
✅ Encoding **categorical variables** (OneHotEncoder, LabelEncoder).  
✅ Addressing **class imbalance** using **ADASYN & SMOTE**.  
✅ **Feature Engineering** – Creating explicit rating bins for Item-Based Filtering.

---

## **🛠 Data Preprocessing**
Before training, several preprocessing steps were applied:

1️⃣ **Handling Outliers** – Using **IQR-based filtering** on price values.  
2️⃣ **Feature Scaling** – Standardizing numerical features with **MinMaxScaler & StandardScaler**.  
3️⃣ **Encoding Categorical Features** – Transforming textual data into machine-readable format.  
4️⃣ **Stratified Sampling** – To ensure balanced training data across all classes.  
5️⃣ **Dimensionality Reduction** – Using **SVD** to optimize collaborative filtering performance.

📌 **Flowchart:**  
![Data Preprocessing Flowchart](https://github.com/user-attachments/assets/shopperlens-preprocessing)

---

## **🧠 Recommendation Models**

### **Branch 1: Memory-Based Model (LightGBM)**
📌 **Approach:**
- Uses **LightGBM** to analyze **session attributes** (color, category, price, etc.).
- Handles **class imbalance** with **ADASYN oversampling**.
- Achieves **80% accuracy** and **AUC score of 0.98**.

📌 **Flowchart:**  
![Branch 1 Flowchart](https://github.com/user-attachments/assets/shopperlens-memory-based)

---

### **Branch 2: Collaborative Filtering (SVD + LightGBM)**
📌 **Approach:**
- Constructs a **user-item interaction matrix** using purchase history.
- Applies **SVD for dimensionality reduction** before training LightGBM.
- Achieves **75% accuracy** and **AUC score of 0.97**.

📌 **Flowchart:**  
![Branch 2 Flowchart](https://github.com/user-attachments/assets/shopperlens-collaborative-filtering)

---

### **Branch 3: Item-Based Filtering (KNN)**
📌 **Approach:**
- Uses **cosine similarity** to recommend similar products.
- Computes **explicit ratings** by binning prices into quantiles.
- Optimizes **KNN hyperparameters (k-neighbors)** for accuracy.
- Achieves **RMSE = 0.4777**, **MAE = 0.3880**.

📌 **Flowchart:**  
![Branch 3 Flowchart](https://github.com/user-attachments/assets/shopperlens-knn)

---

## **📌 Results & Insights**

| **Model** | **Accuracy / RMSE** | **AUC Score** | **Strengths** | **Weaknesses** |
|-----------|-----------------|------------|------------|-------------|
| LightGBM | **80%** | **0.98** | Handles session data well | Limited interpretability |
| SVD + LightGBM | **75%** | **0.97** | Good for collaborative filtering | Struggles with sparse data |
| KNN | **RMSE 0.4777** | N/A | Good for item similarity | Sensitive to K hyperparameter |

📌 **Visualizations:**
- **ROC Curve for LightGBM**
- **Precision-Recall Curve for Collaborative Filtering**
- **Feature Importance Rankings**

---

## **🚀 Future Enhancements**
🔹 **Hybrid Recommendation Approach** – Combining Memory-Based & Collaborative Filtering.  
🔹 **Real-Time Personalization** – Deploying a Flask API for dynamic recommendations.  
🔹 **Feature Engineering** – Integrating user demographics & behavioral analytics.  

---

## **📚 References**
📖 LightGBM Documentation  
📖 Surprise Library for Collaborative Filtering  
📖 Scikit-Learn Documentation  

---

## **📌 Get in Touch**
📧 pranavsharma1395@gmail.com  
📞 +1 (778) 598-6373  
🔗 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  
🔗 [GitHub](https://github.com/user/ShopperLens)  

🚀 *"Optimizing E-Commerce with AI-Powered Personalized Recommendations!"*
