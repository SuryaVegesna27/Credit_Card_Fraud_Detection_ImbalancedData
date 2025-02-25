

# **Credit Card Fraud Detection - Handling Imbalanced Data** 

##  **Project Overview**
This project focuses on detecting fraudulent credit card transactions using **Machine Learning techniques** while addressing the challenges of **highly imbalanced datasets**. The dataset contains **284,807 transactions**, with only **492 fraud cases**, making fraud transactions **0.172%** of the total.

To improve fraud detection, the project implements:
- **Resampling techniques** like **SMOTE (Synthetic Minority Over-sampling Technique)** and **NearMiss Undersampling**.
- **Feature Engineering & Selection** to enhance prediction accuracy.
- **Model Evaluation Metrics** focusing on **Precision, Recall, F1-Score, and AUC-ROC** rather than just accuracy.

---

## 🚀 **How to Run the Project**
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/SuryaVegesna27/Credit_Card_Fraud_Detection_ImbalancedData.git
cd Credit_Card_Fraud_Detection_ImbalancedData
```

### **2️⃣ Install Dependencies**
Create a virtual environment and install the required packages:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### **3️⃣ Run the Jupyter Notebook**
```bash
jupyter notebook notebooks/Credit_Fraud_Analysis.ipynb
```

### **4️⃣ Run the Python Script (if applicable)**
```bash
python src/fraud_detection.py
```

---

## 🛠️ **Machine Learning Techniques Used**
### **1️⃣ Data Preprocessing**
- Handling **missing values** and **data normalization**
- Exploratory Data Analysis (EDA) to understand **feature distributions**
- **Feature Scaling** using `StandardScaler`

### **2️⃣ Handling Imbalanced Data**
- **SMOTE (Synthetic Minority Over-sampling Technique)** to generate synthetic fraud samples.
- **NearMiss Undersampling** to balance the dataset.

### **3️⃣ Model Training & Evaluation**
- **Algorithms Tested:**
  - Logistic Regression
  - Random Forest
  - XGBoost
  - Neural Networks
- **Metrics Used:**
  - **Precision & Recall** (to prioritize fraud detection)
  - **F1-Score** (balance between Precision & Recall)
  - **AUC-ROC** (how well the model distinguishes between fraud & non-fraud)

---

## 📊 **Results & Insights**
| Model                | Precision | Recall | F1-Score | AUC-ROC |
|----------------------|-----------|--------|---------|---------|
| Logistic Regression | **0.84**  | 0.78   | 0.81    | 0.94    |
| Random Forest       | 0.88      | **0.85** | **0.86** | **0.96** |
| XGBoost            | 0.87      | 0.83   | 0.85    | 0.95    |
| Neural Networks    | 0.86      | 0.80   | 0.83    | 0.94    |

✅ **Key Findings:**
- **Random Forest achieved the best balance** between Precision, Recall, and AUC-ROC.
- **SMOTE helped improve recall** (detecting more fraud cases) but slightly increased false positives.
- **Precision-Recall trade-off**: Higher recall means more fraud cases are detected but increases false alarms.

---

## 📜 **Dataset Information**
- **Dataset Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- **Number of Transactions**: `284,807`
- **Number of Fraudulent Transactions**: `492` (`0.172%` of total)
- **Features**:
  - `V1 - V28`: PCA-transformed numerical features
  - `Time`: Seconds elapsed between transactions
  - `Amount`: Transaction amount
  - `Class`: `0 = Legitimate`, `1 = Fraud`

---

## 📌 **Key Takeaways**
✅ **Handling class imbalance is critical** for fraud detection models.  
✅ **AUC-ROC & Recall** are better evaluation metrics than accuracy.  
✅ **Random Forest & XGBoost** performed best for fraud detection.  
✅ **Feature engineering & resampling techniques improve model performance.**

---

## 🤝 **Contributing**
If you’d like to contribute, feel free to **submit a pull request** or report any issues.

---

## 🔗 **References**
- Kaggle Dataset: [Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- Imbalanced Data Handling: **SMOTE & NearMiss**  
- Model Evaluation: **Precision, Recall, AUC-ROC**

---

## 📜 **License**
This project is licensed under the **MIT License**.
