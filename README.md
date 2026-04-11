## 📌 Project Title

**Heart Disease Prediction using Machine Learning (TAE-I Project)**

---

## 👩‍💻 Team Members

* **Tisha Mondal (CS23059)**
* **Akshad Jaiswal (CS23057)**

---

## 🏫 Institute Details

S. B. Jain Institute of Technology, Management & Research, Nagpur
Semester: 6th (Third Year)
Session: 2025–26

---

## 📌 Project Description

Heart disease is one of the leading causes of death worldwide. Early prediction of heart disease can help in timely diagnosis and treatment, reducing the risk of severe health complications.

This project focuses on building a **Machine Learning-based Heart Disease Prediction System** using the **UCI Heart Disease Dataset**. The system analyzes patient medical data such as age, cholesterol, blood pressure, etc., and predicts whether the person is likely to have heart disease.

A total of **6 Machine Learning models** are implemented and compared to determine the best-performing model.

---

## 🎯 Objective

* To implement and compare multiple ML models
* To analyze model performance using different metrics
* To identify the most accurate model for prediction
* To understand the role of preprocessing in ML

---

## 📊 Dataset Information

* **Dataset Name:** UCI Heart Disease Dataset
* **Source:** Kaggle / UCI Repository
* **Records:** ~300
* **Features:** 13 input features + 1 target

### Target Variable:

* `0 → No Heart Disease`
* `1 → Heart Disease Present`

---

## ⚙️ Models Implemented

### 👩‍💻 Tisha Mondal:

* Decision Tree
* Support Vector Machine (SVM)
* Naive Bayes

### 👨‍💻 Akshad Jaiswal:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Random Forest

---

## 🧠 Final Combined Analysis

A separate notebook (**Heart_Disease_Complete_Model_Analysis.ipynb**) was created to:

* Combine all models
* Compare performance
* Generate graphs & evaluation metrics

---

## ⚙️ Implementation Details

### 🔹 Libraries Used

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

### 🔹 Steps Performed

#### 1. Data Loading

* Dataset loaded from GitHub using URL

#### 2. Data Preprocessing

* Dropped unnecessary column (`id`)
* Converted target variable into binary
* Handled missing values using **SimpleImputer**
* Applied **One-Hot Encoding**
* Feature scaling using **StandardScaler**

---

#### 3. Exploratory Data Analysis (EDA)

* Count plot for target variable
* Correlation heatmap
* Data summary (`info`, `describe`)

---

#### 4. Model Training

Models used:

* Decision Tree
* SVM
* Naive Bayes
* Logistic Regression
* KNN
* Random Forest

---

#### 5. Model Evaluation

Metrics used:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC Curve
* Precision-Recall Curve

---

#### 6. Train-Test Splits Used

* **80:20**
* **70:30**

---

#### 7. Visualization

* Confusion matrices for all models
* Bar graphs for performance comparison
* ROC curve comparison
* Accuracy comparison graph
* Heatmap for model performance

---

## 📈 Results Summary

* **Best Performing Models:**

  * Logistic Regression (~90%)
  * Random Forest (~88%)
  * SVM (~85%)

* **Lowest Performance:**

  * Naive Bayes

* Models perform better with **more training data (80:20 split)**

---

## ▶️ How to Run the Project (Step-by-Step)

### 🔹 Step 1: Clone Repository

```bash
git clone https://github.com/akshadjaiswal005/Heart-disease-prediction.git
cd Heart-disease-prediction
```

---

### 🔹 Step 2: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

### 🔹 Step 3: Open Notebooks

Use either:

👉 Google Colab
👉 Jupyter Notebook

```bash
jupyter notebook
```

---

### 🔹 Step 4: Run Individual Models

* Open files inside `Tisha_Models` folder:

  * Decision Tree
  * SVM
  * Naive Bayes

* Open other notebooks:

  * Logistic Regression
  * KNN
  * Random Forest

Run all cells step-by-step

---

### 🔹 Step 5: Run Final Analysis

Open:

```
Heart_Disease_Complete_Model_Analysis.ipynb
```

Run all cells to:

* Compare models
* Generate graphs
* View results

---

## 📂 Project Structure

```
Heart-disease-prediction/
│── heart_disease_uci.csv
│── Tisha_Models/
│   ├── Decision Tree Model
│   ├── SVM Model
│   ├── Naive Bayes Model
│── KNN_model.ipynb
│── logistic_regression_model.ipynb
│── random_forest_model.ipynb
│── Heart_Disease_Complete_Model_Analysis.ipynb
│── README.md
```

---

## 📌 Conclusion

This project demonstrates that Machine Learning can effectively predict heart disease using clinical data.

* Logistic Regression and Random Forest performed best
* Data preprocessing significantly improved accuracy
* Increasing training data improved model performance

---

## 🔮 Future Scope

* Use larger datasets
* Apply Deep Learning models
* Deploy as web app (Flask/Streamlit)
* Add real-time prediction system

---

## 📚 Reference

Based on final project report 

---

## 👩‍💻 Developed By

* Tisha Mondal
* Akshad Jaiswal


