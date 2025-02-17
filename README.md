# 🚀 ShopperLens: Intelligent Personalized Recommendation System

![ShopperLens Banner](https://github.com/user-attachments/assets/fee9463f-1f6c-4e95-814a-925fbc5d63e5)

---

## 🌟 Project Overview
**ShopperLens** is an advanced AI-powered recommendation system designed to enhance the online shopping experience through **personalized product suggestions**. By leveraging **machine learning and data-driven analytics**, ShopperLens delivers **highly relevant recommendations** to users based on their behavior, past purchases, and session interactions.


### 🔥 **Key Features**
✅ **Three-Branch Model Architecture**: Memory-Based, Collaborative Filtering, and Item-Based approaches.
✅ **Hyperparameter-Tuned Models**: LightGBM, SVD, and KNN for enhanced performance.
✅ **Data Preprocessing & Feature Engineering**: Handling imbalances, encoding categorical data, and scaling numerical values.
✅ **User-Centric Testing**: Sample data inputs showcase real-time recommendation workflow.
✅ **Optimized Performance**: Model evaluation metrics guide model selection and refinements.

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
5. [📡 Model Architecture](#-model-architecture)
- [Branch 1: Memory-Based Learning (LightGBM)](#-branch-1-memory-based-learning-lightgbm)
- [Branch 2: Collaborative Filtering (SVD + LightGBM)](#-branch-2-collaborative-filtering-svd--lightgbm)
- [Branch 3: Item-Based Filtering (KNN)](#-branch-3-item-based-filtering-knn)
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
The dataset used is **E-Shop Clothing 2008**, consisting of **shopping behavior data collected from an online retail store**. 
([UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/553/clickstream+data+for+online+shopping)).
It includes:
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
## 🛠 Model Architecture
ShopperLens follows a **multi-branch modeling approach**, consisting of:
- 1️⃣ **Memory-Based Model (LightGBM)** – Analyzes session attributes.
- 2️⃣ **Collaborative Filtering (SVD + LightGBM)** – Learns user-item interaction patterns.
- 3️⃣ **Item-Based Filtering (KNN)** – Recommends similar products using cosine similarity.

📌 **Overall System Flowchart**  
![Overall Model Flow](https://github.com/user-attachments/assets/shopperlens-overall-flowchart)

### **Branch 1: Memory-Based Learning (LightGBM)**
- **Objective:** Predict user preferences based on session attributes.
- **Hyperparameters:** `max_depth=3, n_estimators=4, learning_rate=0.06`
- **Result:** Achieved **80% accuracy** and **AUC score of 0.98**.
- **Use Case:** Works well for users with clear session behavior.

📌 **Flowchart:**  
![Memory-Based Flowchart](https://github.com/user-attachments/assets/shopperlens-memory-based)

### **Branch 2: Collaborative Filtering (SVD + LightGBM)**
- **Objective:** Learn user-item relationships for recommendations.
- **Hyperparameters:** `SVD + LightGBM for further refinement`
- **Result:** Achieved **75% accuracy** and **AUC score of 0.97**.
- **Use Case:** Useful for repeat customers with historical data.

📌 **Flowchart:**  
![Collaborative Filtering Flowchart](https://github.com/user-attachments/assets/shopperlens-collaborative-filtering)

### **Branch 3: Item-Based Filtering (KNN)**
- **Objective:** Find similar products based on cosine similarity.
- **Hyperparameters:** `K=10 neighbors`
- **Result:** Achieved **RMSE = 0.4777, MAE = 0.3880**.
- **Use Case:** Ideal for similar product suggestions.

📌 **Flowchart:**  
![Item-Based Flowchart](https://github.com/user-attachments/assets/shopperlens-knn)

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
