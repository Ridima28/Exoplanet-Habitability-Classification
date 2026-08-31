# 🪐 Exoplanet Habitability Classification

> **Can Machine Learning find patterns that distinguish potentially habitable worlds? 🌌**

A Machine Learning project that classifies exoplanets into different habitability categories using **real astronomical data** from the **NASA Exoplanet Archive / Planetary Habitability Laboratory dataset**.

The project explores data preprocessing, exploratory data analysis, feature selection, class balancing, model comparison, and hyperparameter tuning.

---

## 🎯 Project Overview

The target variable is **`P_HABITABLE`**, treated as a multiclass classification problem.

The model classifies exoplanets into:

* **Class 0** — Inhabitable
* **Class 1** —  Potentially Habitable
* **Class 2** — Positively Habitable

The original dataset contained **4,048 observations and 112 features**.

---

## 📊 Model Results


| Model             | Accuracy | Precision | Recall | F1 Score | Time Taken (s) |
|-------------------|----------|-----------|--------|----------|----------------|
| Decision Tree     | 90.68%   | 92.79%    | 90.56% | 90.46%   | 0.002650       |
| Gradient Boosting | 90.68%   | 92.79%    | 90.56% | 90.46%   | 0.323745       |
| **KNN**           | **98.34%** | **98.40%** | **98.36%**     | **98.34%**| **0.094308** |

### 🏆 Best Model

**K-Nearest Neighbor**

Although the Decision Tree had the fastest execution time, KNN provides a much better balance between **classification performance and execution time**.


---

## 🔬 Feature Selection

Feature selection was an important part of the project.

The original dataset contained **112 features**, including planetary, stellar, and derived characteristics.

Features were analyzed using:

* Correlation analysis
* Random Forest feature importance
* Ada Boost Classifier
* Feature selection techniques

The final model was built using a smaller set of relevant **raw physical measurements**, avoiding features that could introduce target leakage.

---


## 🔄 Machine Learning Pipeline

```text
Real Exoplanet Dataset
        ↓
Exploratory Data Analysis
        ↓
Missing Value Analysis
        ↓
Class Imbalance Analysis
        ↓
Data Resampling
        ↓
Feature Selection
        ↓
Train / Test Split
        ↓
Multiple ML Models
        ↓
GridSearchCV
        ↓
Final KNN
        ↓
Evaluation
```

---

## 🛠️ Techniques & Libraries

### Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* ELI5

### Techniques

* Exploratory Data Analysis
* Data preprocessing
* Class balancing
* Feature selection
* Random Forest Feature Importance
* Permutation Importance
* MinMax scaler
* Multiclass Classification
* GridSearchCV
* Confusion Matrix

---


## ⚠️ Limitations

This project is **not a definitive habitability detector**.

Actual planetary habitability depends on many factors, including atmospheric composition, surface conditions, radiation environment, magnetic fields, and other characteristics that aren't fully represented in this dataset.

Therefore, the model's accuracy reflects its ability to classify the **available dataset labels**, not certainty that an exoplanet can support life.

---

## 📈 Key Takeaways

* Real astronomical datasets can be highly imbalanced and contain substantial missing data.
* Feature selection can be as important as model selection.
* High accuracy should always be investigated for possible data leakage.
* Ensemble models can perform strongly on structured astronomical data.
* Domain knowledge is important when deciding which features make scientific sense.

---

## 📦 Installation

```bash
git clone https://github.com/Ridima28/exoplanet-habitability.git

cd exoplanet-habitability-classification


```

### Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
eli5
```

---

## 📁 Project Structure

```text
exoplanet-habitability/
│
├── images/
│
├── models/
│   └── model.ipynb
│   └── model.pkl
│   └── phl_exoplanet_catalog_2019.csv
│  
└── README.md
```

---

## 📚 Dataset

**Dataset:** PHL Exoplanet Catalog
**Source:** Planetary Habitability Laboratory / NASA-related astronomical data

The dataset contains planetary and stellar parameters used to study exoplanet habitability.

---

## 🚀 Future Improvements

* Add more scientifically relevant planetary parameters
* Improve missing-value handling
* Explore SHAP for explainability
* Test additional ensemble methods
* Incorporate newer exoplanet observations
* Build an interactive prediction interface

---

## 👩‍💻 Author

**Ridima**

**Machine Learning × Astronomy 🪐🌌**

Interested in applying Machine Learning to **astronomy, Earth/space science, and scientific problems**.

---

⭐ **If you found this project interesting, consider starring the repository!**