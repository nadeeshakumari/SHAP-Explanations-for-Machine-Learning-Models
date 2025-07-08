# 🔍 SHAP Explanations for Machine Learning Classification Models

This repository provides code to generate and visualize SHAP (SHapley Additive exPlanations) values for various machine learning classification models. SHAP is used to interpret the impact of features on model predictions, offering insight into how models make decisions.

## 🚀 Features

- Supports SHAP explanations for multiple classification models  
- Uses `TreeExplainer` for tree-based models for fast, exact explanations  
- Uses `KernelExplainer` for non-tree-based models for model-agnostic explanations  
- Provides global and local interpretations  
- Easily adaptable to any trained classification model and dataset  


📂 How to Use
- Train the classification model as usual.

- Import the SHAP explanation functions and call them.

- The function will generate SHAP summary bar plots, beeswam plots, decision plots, waterfall plots, heatmap, dot plot etc.


🔍 Explanation Details
- For tree-based models (Random Forest, XGBoost, LightGBM, CatBoost, Gradient Boosting), the code uses shap.TreeExplainer which is fast and accurate.

- For non-tree models (Logistic Regression, SVM, Naive Bayes, KNN, MLP), the code uses shap.KernelExplainer which is model-agnostic but slower. It uses a sample of the training data as the background distribution.

♻️ Customization
- Change the number of background samples for KernelExplainer to balance speed and accuracy.

- Extend to multiclass or regression models with minor modifications.


