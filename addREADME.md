

# Heart Disease Prediction

## Project Overview
Predict heart disease presence (0/1) using multiple machine learning algorithms on UCI Heart Disease dataset.

## 🧠Algorithms Implemented
- Logistic Regression (primary for binary classification)
- Random Forest
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Naive Bayes
- Decision Tree

## 📊Key Results (80:20 Split)

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| **Logistic Regression** | **0.900** | **0.880** | **0.88** | **0.880** |
| SVM | 0.850 | 0.833 | 0.80 | 0.816 |
| Decision Tree | 0.817 | 0.769 | 0.80 | 0.784 |
| Naive Bayes | 0.600 | 1.000 | 0.84 | 0.077 |

## 🔧 Implementation Steps

### 1. Setup
```bash
pip install pandas scikit-learn numpy
```

### 2. Load & Preprocess Data
```python
import pandas as pd
from sklearn.preprocessing import OneHotEncoder

df = pd.read_csv('heart_disease_uci.csv')

# One-Hot Encoding for categorical variables
categorical_cols = ['sex', 'cp', 'restecg', 'slope', 'thal']
df_encoded = pd.get_dummies(df, columns=categorical_cols, drop_first=True)
```

### 3. Train Logistic Regression (Binary: 0/1)
```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score

X = df_encoded.drop('target', axis=1)
y = df_encoded['target']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

model = LogisticRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)  # Outputs: 0 or 1

print(f"Accuracy: {accuracy_score(y_test, predictions):.3f}")
```

### 4. Train Other Models (Same Pattern)
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.svm import SVC

models = {
    'Random Forest': RandomForestClassifier(),
    'KNN': KNeighborsClassifier(),
    'SVM': SVC()
}

for name, model in models.items():
    model.fit(X_train, y_train)
    print(f"{name}: {accuracy_score(y_test, model.predict(X_test)):.3f}")
```

## 📁 Project Structure
```
Heart_disease_prediction/
└── Heart/Tisha_Models/
    ├── logistic_regression_model.ipynb
    ├── random_forest_model.ipynb
    ├── KNN_model.ipynb
    ├── Heart_Disease_Complete_Model_Analysis.ipynb
    └── heart_disease_uci.csv
```
Methodology
Data loading using GitHub-hosted dataset
Data preprocessing (handling missing values, encoding, scaling)
Model training and testing
Performance evaluation using:
Accuracy Score
Confusion Matrix
Classification Report
Each model is evaluated using two different train-test splits:

80:20 (Training:Testing)
70:30 (Training:Testing)
This allows comparison of model performance under varying data conditions.

Repository Structure
Individual model implementations are organized into separate notebooks
Final combined notebook includes all models and comparative evaluation
Dataset is stored in the repository and accessed via raw GitHub link
Tools and Technologies
Python
Pandas, NumPy
Scikit-learn
Matplotlib, Seaborn
Google Colab
GitHub (for collaboration and version control)
Collaboration
This project is developed collaboratively as part of Machine Learning TAE-1.

Tisha Mondal – Decision Tree, SVM, Naive Bayes
Akshad Jaiswal – Logistic Regression, KNN, Random Forest

## 💡 Quick Start for New Users

1. **Clone & navigate**
```bash
git clone <your-repo-url>
cd Heart_disease_prediction/Heart/Tisha_Models
```

2. **Run any notebook** (Jupyter/Colab)
   - Start with `logistic_regression_model.ipynb`
   - Then explore other model notebooks

3. **Key observation**: Logistic Regression works best for this binary classification problem

## 📝 Notes
- All categorical features require One-Hot Encoding before training
- Target variable is binary (0 = No disease, 1 = Disease)
- Models are evaluated on Accuracy, Precision, Recall, and F1 Score

---

