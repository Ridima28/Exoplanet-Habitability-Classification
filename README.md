Absolutely — based on your notebook, I’d keep the README **clean, project-focused, and GitHub-friendly**, without documenting every single preprocessing step.

# 🌌 Exoplanet Habitability Classification

A machine learning project that classifies exoplanets based on their potential habitability using observational and planetary data from the **PHL Exoplanet Catalog (2019)**.

The project explores different classification algorithms, handles missing data and class imbalance, performs feature selection, and compares multiple machine learning models to identify the best-performing approach.

## 🎯 Objective

The goal is to classify exoplanets into three categories:

* 🌍 **Habitable**
* 🟡 **Potentially Habitable**
* ❌ **Not-Habitable**

The dataset contains **4,048 exoplanets and 112 features**, including planetary properties, stellar characteristics, orbital parameters, and habitability-related attributes.

## 🧠 Machine Learning Workflow

The project follows a typical end-to-end classification pipeline:

1. **Data Exploration & Analysis**

   * Dataset structure and feature analysis
   * Missing-value analysis
   * Exploratory visualization

2. **Data Preprocessing**

   * Handling missing values
   * Encoding categorical features
   * Feature preparation
   * Standardization where required

3. **Class Imbalance Handling**

   * Applied **SMOTE** to balance the training data.

4. **Feature Selection**

   * Used **Random Forest feature importance** to identify influential features.

5. **Model Training & Hyperparameter Tuning**

   * Grid Search
   * Randomized Search
   * 5-fold cross-validation

6. **Model Evaluation**

   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Classification report
   * Confusion matrix

## 🤖 Models Compared

* Decision Tree
* Random Forest
* K-Nearest Neighbors
* Logistic Regression
* Support Vector Machine
* Stochastic Gradient Descent
* Gaussian Naive Bayes

## 📊 Results

| Model               |   Accuracy | Weighted F1 |
| ------------------- | ---------: | ----------: |
| 🥇 Random Forest    | **98.26%** |  **98.27%** |
| Decision Tree       |     95.79% |      95.83% |
| SVM                 |     81.00% |      81.45% |
| Logistic Regression |     73.89% |      73.73% |
| SGD                 |     72.99% |      72.19% |
| Naive Bayes         |     61.00% |      58.87% |
| KNN                 |     33.52% |      16.83% |

### 🏆 Best Model: Random Forest

Random Forest achieved the best overall performance with:

* **Accuracy:** 98.26%
* **Precision:** 98.29%
* **Recall:** 98.27%
* **F1-score:** 98.27%

Class-wise performance was also strong, with F1-scores around **0.98–0.99** across all three classes.

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* Jupyter Notebook

## 📁 Project Structure

```text
Exoplanet-Habitability-Classification/
│
├── main.ipynb
├── phl_exoplanet_catalog_2019.csv
└── README.md
```

## 🚀 How to Run

Clone the repository:

```bash
git clone <your-repository-url>
cd Exoplanet-Habitability-Classification
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

Run the notebook:

```bash
jupyter notebook main.ipynb
```

## 🔭 Key Takeaway

This project demonstrates how classical machine learning techniques can be applied to astronomical data to investigate patterns related to exoplanet habitability.

It also provided practical experience with **imbalanced classification, feature selection, hyperparameter tuning, cross-validation, and ensemble learning**.
