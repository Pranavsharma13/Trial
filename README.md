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
--------------------------
-----------------------
---------------
-------------------


# 🚀 ShopperLens: AI-Driven Personalized Recommendation System

![ShopperLens Banner](https://github.com/user-attachments/assets/shopperlens-banner)

---

## 🌟 Project Overview
**ShopperLens** is an advanced AI-powered recommendation system designed to enhance the online shopping experience through **personalized product suggestions**. By leveraging **machine learning and data-driven analytics**, ShopperLens delivers **highly relevant recommendations** to users based on their behavior, past purchases, and session interactions.

### 🔥 **Key Features**
✅ **Multi-Model Approach**: Utilizes Memory-Based, Collaborative Filtering, and Item-Based strategies.  
✅ **User & Item-Based Predictions**: Ensures highly personalized recommendations.  
✅ **Scalable & Efficient**: Designed to process large datasets efficiently.  
✅ **Real-Time Personalization**: Future integration with API-based recommendation delivery.

### 🏗 **Tech Stack**
🚀 **Languages**: Python  
📊 **Libraries**: LightGBM, Scikit-learn, Pandas, NumPy, Seaborn, Surprise, Matplotlib  
🛠 **Tools**: Jupyter Notebook, GitHub, Flask (for deployment), FastAPI  

---

## 📌 Table of Contents
1. [🚀 Project Motivation](#-project-motivation)
2. [📊 Dataset Overview](#-dataset-overview)
3. [🛠 Data Preprocessing](#-data-preprocessing)
4. [🧠 How It Works](#-how-it-works)
5. [📡 Model Architecture](#-model-architecture)
6. [📊 Performance Metrics](#-performance-metrics)
7. [💡 Key Insights](#-key-insights)
8. [🚀 Future Enhancements](#-future-enhancements)
9. [📚 References](#-references)

---

## 🚀 Project Motivation
E-commerce platforms face challenges in delivering **highly relevant recommendations** due to:
- **Sparse user-item interaction data**, affecting prediction accuracy.
- **Cold start problem** for new users and products.
- **Balancing personalization vs. diversity** in suggestions.

ShopperLens tackles these issues by employing a **multi-model recommendation system** that improves accuracy and engagement.

---

## 📊 Dataset Overview
The dataset used is **E-Shop Clothing 2008**, consisting of **shopping behavior data collected from an online retail store**. It includes:
✔ **User Sessions** – Tracks clicks, views, and purchase interactions.  
✔ **Product Attributes** – Details such as color, category, price, metadata.  
✔ **Transaction History** – Captures orders, session IDs, and timestamps.  

### 🏗 **Data Processing Steps**
🔹 **Handling Missing Values** – Using Mean/Mode imputation.  
🔹 **Encoding Categorical Variables** – Applying OneHotEncoder & LabelEncoder.  
🔹 **Balancing Data** – Addressing class imbalance with **ADASYN & SMOTE**.  
🔹 **Feature Engineering** – Generating explicit rating bins for Item-Based Filtering.  

📌 **Flowchart:**  
![Data Preprocessing Flowchart](https://github.com/user-attachments/assets/shopperlens-preprocessing)

---

## 🧠 How It Works
ShopperLens employs **three different recommendation strategies**, each optimized for different use cases:

### **1️⃣ Memory-Based Learning (LightGBM)**
✔ **Analyzes session attributes** such as color, category, and price.
✔ **Handles class imbalance** using ADASYN oversampling.
✔ **Achieves 80% accuracy, AUC score of 0.98**.

📌 **Flowchart:**  
![Memory-Based Flowchart](https://github.com/user-attachments/assets/shopperlens-memory-based)

### **2️⃣ Collaborative Filtering (SVD + LightGBM)**
✔ **Creates a user-item interaction matrix** based on past purchases.
✔ **Uses Singular Value Decomposition (SVD) for dimensionality reduction.**
✔ **Achieves 75% accuracy, AUC score of 0.97**.

📌 **Flowchart:**  
![Collaborative Filtering Flowchart](https://github.com/user-attachments/assets/shopperlens-collaborative-filtering)

### **3️⃣ Item-Based Filtering (KNN Similarity)**
✔ **Computes cosine similarity** between different products.
✔ **Utilizes explicit ratings (price quantiles) to refine recommendations.**
✔ **Achieves RMSE = 0.4777, MAE = 0.3880**.

📌 **Flowchart:**  
![Item-Based Flowchart](https://github.com/user-attachments/assets/shopperlens-knn)

---

## 📡 Model Architecture
ShopperLens follows a **multi-branch architecture**, consisting of:
1️⃣ **Data Preprocessing Pipeline** – Handles missing values, encoding, and class balancing.  
2️⃣ **Feature Engineering** – Generates derived features for improved model performance.  
3️⃣ **Model Training & Optimization** – LightGBM, SVD, and KNN-based approaches.  

📌 **Architecture Diagram:**
![System Architecture](https://github.com/user-attachments/assets/shopperlens-architecture)

---

## 📊 Performance Metrics
| **Model** | **Accuracy / RMSE** | **AUC Score** | **Strengths** | **Weaknesses** |
|-----------|-----------------|------------|------------|-------------|
| LightGBM | **80%** | **0.98** | Session-based, high accuracy | Limited interpretability |
| SVD + LightGBM | **75%** | **0.97** | Works well with sparse data | Cold start issue |
| KNN | **RMSE 0.4777** | N/A | Finds similar products | Sensitive to K hyperparameter |

---

## 💡 Key Insights
📌 **Memory-Based Learning** provides high accuracy but requires well-defined session attributes.  
📌 **Collaborative Filtering** captures hidden patterns but is affected by data sparsity.  
📌 **Item-Based Filtering** is highly interpretable but sensitive to hyperparameter tuning.  

---

## 🚀 Future Enhancements
🔹 **Hybrid Approach** – Combining Memory-Based and Collaborative Filtering for enhanced recommendations.  
🔹 **Real-Time API** – Deploying a Flask or FastAPI-based API for live recommendations.  
🔹 **Feature Engineering Enhancements** – Incorporating user demographics and behavioral analytics.  

---

## 📚 References
📖 LightGBM Documentation  
📖 Surprise Library for Collaborative Filtering  
📖 Scikit-Learn Documentation  

---

## 📌 Get in Touch
📧 pranavsharma1395@gmail.com  
📞 +1 (778) 598-6373  
🔗 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  
🔗 [GitHub](https://github.com/user/ShopperLens)  

🚀 *"Optimizing E-Commerce with AI-Powered Personalized Recommendations!"*
===================================
===================================

=================================
==============================


# 🚀 ShopperLens: AI-Driven Personalized Recommendation System

![ShopperLens Banner](https://github.com/user-attachments/assets/shopperlens-banner)

---

## 🌟 Project Overview
**ShopperLens** is an advanced AI-powered recommendation system designed to enhance the online shopping experience through **personalized product suggestions**. By leveraging **machine learning and data-driven analytics**, ShopperLens delivers **highly relevant recommendations** to users based on their behavior, past purchases, and session interactions.

### 🔥 **Key Features**
✅ **Multi-Model Approach**: Utilizes Memory-Based, Collaborative Filtering, and Item-Based strategies.  
✅ **User & Item-Based Predictions**: Ensures highly personalized recommendations.  
✅ **Scalable & Efficient**: Designed to process large datasets efficiently.  
✅ **Real-Time Personalization**: Future integration with API-based recommendation delivery.

### 🏗 **Tech Stack**
🚀 **Languages**: Python  
📊 **Libraries**: LightGBM, Scikit-learn, Pandas, NumPy, Seaborn, Surprise, Matplotlib  
🛠 **Tools**: Jupyter Notebook, GitHub, Flask (for deployment), FastAPI  

---

## 📌 Table of Contents
1. [🚀 Project Motivation](#-project-motivation)
2. [📊 Dataset Overview](#-dataset-overview)
3. [📈 Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
4. [🛠 Data Preprocessing](#-data-preprocessing)
5. [🧠 How It Works](#-how-it-works)
6. [📡 Model Architecture](#-model-architecture)
7. [🧪 Sample Data & Testing](#-sample-data--testing)
8. [📊 Performance Metrics](#-performance-metrics)
9. [💡 Key Insights](#-key-insights)
10. [🚀 Future Enhancements](#-future-enhancements)
11. [📚 References](#-references)

---

## 🚀 Project Motivation
E-commerce platforms face challenges in delivering **highly relevant recommendations** due to:
- **Sparse user-item interaction data**, affecting prediction accuracy.
- **Cold start problem** for new users and products.
- **Balancing personalization vs. diversity** in suggestions.

ShopperLens tackles these issues by employing a **multi-model recommendation system** that improves accuracy and engagement.

---

## 📊 Dataset Overview
The dataset used is **E-Shop Clothing 2008**, consisting of **shopping behavior data collected from an online retail store**. It includes:
✔ **User Sessions** – Tracks clicks, views, and purchase interactions.  
✔ **Product Attributes** – Details such as color, category, price, metadata.  
✔ **Transaction History** – Captures orders, session IDs, and timestamps.  

### 📌 Data Processing Steps
🔹 **Handling Missing Values** – Using Mean/Mode imputation.  
🔹 **Encoding Categorical Variables** – Applying OneHotEncoder & LabelEncoder.  
🔹 **Balancing Data** – Addressing class imbalance with **ADASYN & SMOTE**.  
🔹 **Feature Engineering** – Generating explicit rating bins for Item-Based Filtering.  

📌 **Flowchart:**  
![Data Preprocessing Flowchart](https://github.com/user-attachments/assets/shopperlens-preprocessing)

---

## 📈 Exploratory Data Analysis (EDA)
Before training the models, we conducted **EDA to understand data distributions, patterns, and correlations**.

### 📊 Key Findings
- **Most frequently purchased product categories** were analyzed.
- **Price distribution across different countries** was visualized.
- **User behavior trends** were identified through session duration analysis.
- **Feature correlations** were analyzed to select the most impactful attributes for modeling.

📌 **Visualizations:**
- **Purchase Frequency Distribution**
- **Top Selling Product Categories**
- **Feature Correlation Heatmap**

![EDA Visualization](https://github.com/user-attachments/assets/shopperlens-eda)

---

## 🧪 Sample Data & Testing
ShopperLens uses sample test cases to **validate recommendation accuracy**.

### 📌 Sample Test Case Workflow:
1️⃣ **New User Data Input** – Generates recommendations based on limited session history.  
2️⃣ **Session-Based Predictions** – Provides product recommendations using LightGBM.  
3️⃣ **Personalized Recommendation Output** – Displays top predicted products based on model rankings.  

📌 **Sample Code Execution:**
```python
new_data_point = pd.DataFrame({
    'year': [2008], 'month': [5], 'day': [10], 'price': [20],
    'order': [3], 'country': [1], 'page 1 (main category)': [2],
    'page 2 (clothing model)': ['A11'], 'location': [2],
    'model photography': [1], 'price 2': [1], 'page': [2]
})
recommendations = lgb_model.predict(preprocessor.transform(new_data_point))
print("Recommended Product Colors:", recommendations)
```
📌 **Visualization of Recommendations:**
![Recommendation Output](https://github.com/user-attachments/assets/shopperlens-recommendations)

---

## 📡 Model Architecture
The system consists of **three distinct recommendation branches:**
1️⃣ **Memory-Based Model (LightGBM)** – Analyzes session attributes.  
2️⃣ **Collaborative Filtering (SVD + LightGBM)** – Learns user-item interaction patterns.  
3️⃣ **Item-Based Filtering (KNN)** – Recommends similar products using cosine similarity.

📌 **Architecture Diagram:**
![System Architecture](https://github.com/user-attachments/assets/shopperlens-architecture)

---

## 📊 Performance Metrics
| **Model** | **Accuracy / RMSE** | **AUC Score** | **Strengths** | **Weaknesses** |
|-----------|-----------------|------------|------------|-------------|
| LightGBM | **80%** | **0.98** | Session-based, high accuracy | Limited interpretability |
| SVD + LightGBM | **75%** | **0.97** | Works well with sparse data | Cold start issue |
| KNN | **RMSE 0.4777** | N/A | Finds similar products | Sensitive to K hyperparameter |

---

## 💡 Key Insights
📌 **Memory-Based Learning** provides high accuracy but requires well-defined session attributes.  
📌 **Collaborative Filtering** captures hidden patterns but is affected by data sparsity.  
📌 **Item-Based Filtering** is highly interpretable but sensitive to hyperparameter tuning.  

---

## 🚀 Future Enhancements
🔹 **Hybrid Approach** – Combining Memory-Based and Collaborative Filtering.  
🔹 **Real-Time API Deployment** – Flask/FastAPI for live recommendations.  
🔹 **Enhanced Feature Engineering** – Incorporating behavioral analytics.

---

## 📚 References
📖 LightGBM Documentation  
📖 Surprise Library for Collaborative Filtering  
📖 Scikit-Learn Documentation  

---

## 📌 Get in Touch
📧 pranavsharma1395@gmail.com  
📞 +1 (778) 598-6373  
🔗 [LinkedIn](https://www.linkedin.com/in/pranav-harish-sharma/)  
🔗 [GitHub](https://github.com/user/ShopperLens)  

🚀 *"Optimizing E-Commerce with AI-Powered Personalized Recommendations!"*
