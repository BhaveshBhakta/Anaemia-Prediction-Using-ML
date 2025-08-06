## Anaemia Prediction

### Project Overview

This project aims to predict the **presence of anaemia** based on a minimal set of health indicators, including haemoglobin (Hb) levels and color-based features derived from a finger prick test (represented by percentage of red, green, and blue pixels). The goal is to develop a simple yet accurate machine learning model that can assist in the preliminary screening for anaemia.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Anaemia Prediction](https://www.kaggle.com/datasets/humairmunir/anaemia-prediction)
  * **Size**: 104 entries, 7 columns
  * **Key Features**:
      * Sex, %Red Pixel, %Green pixel, %Blue pixel, Hb.
  * **Approach**:
      * Data Cleaning: Dropped the `Number` column as it is a unique identifier. No missing values or duplicates were found.
      * Exploratory Data Analysis: Histograms, Boxplots, and a heatmap were used for visualization to understand data distributions and correlations.
      * Label Encoding: Applied to all columns, including numerical ones (as per the notebook) and the target 'Anaemic'.
      * Binary Classification: The target variable 'Anaemic' indicates whether an individual is anaemic ('Yes') or not ('No').
      * Models Used:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 100% across all models (Logistic Regression, Ridge Classifier, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVC).
      * The extremely high accuracies suggest that the features, particularly haemoglobin (Hb) level, are highly predictive of anaemia, or there may be a data leakage issue.

-----

### Purpose and Applications

  * Assist in the **preliminary screening for anaemia** using non-invasive or minimal-invasive methods.
  * Provide a cost-effective and rapid tool for health workers in resource-limited settings.
  * Facilitate early diagnosis and treatment of anaemia.
  * Serve as a tool for educational purposes in health and data science.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Anaemia-Prediction-Using-ML.git
cd Anaemia-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Thoroughly investigating the 100% accuracy to ensure no data leakage or overfitting is present. In medical datasets, such high performance is rare and warrants close inspection.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models to ensure robustness.
  * Exploring the impact of different feature selection or transformation techniques, especially on the pixel data.
  * Adding explainability (e.g., SHAP or LIME) to understand which features are the most critical for anaemia prediction.
