# Telecom Churn Prediction Project

This project analyzes and predicts customer churn using a telecom dataset from Kaggle: [Telecom Churn Datasets](https://www.kaggle.com/datasets/mnassrib/telecom-churn-datasets).

<p style="color:red;"><b>Warning</b>: GitHub's Jupyter Notebook renderer does not display the complete notebook. Please use <a href="https://nbviewer.org/github/prabhsl/Telecom-Churn-EDA-and-Predictive-Modeling/blob/main/Telecom%20Churn.ipynb">this nbviewer link</a> to view the notebook properly, or alternatively, download the notebook and open it in your preferred code editor.</p>

---

## Project Overview

This repository details a project focused on understanding and predicting customer churn in a telecom dataset. We utilized Python with popular libraries like `pandas`, `sklearn`, `matplotlib`, and `seaborn` for the entire process, from data loading to machine learning model training.

### Key Steps:

1.  **Data Loading & Initial Inspection**: Loaded `churn-bigml-80.csv` and performed initial checks, noting potential outliers.
2.  **Exploratory Data Analysis (EDA)**: Investigated relationships between features and churn.
    * **Categorical Features**: Found customers with **international plans** had a significantly **higher churn rate** (~43.7%), while those with **voice mail plans** showed a **lower churn rate** (~8.9%).
    * **Numerical Features**: Identified that increased **daytime usage** and frequent **customer service calls** were strong indicators of higher churn risk.
3.  **Data Preprocessing**: Prepared the data for modeling, including encoding categorical features and splitting into training/testing sets.
4.  **Predictive Modeling**: Selected tree-based classifiers (Random Forest and Decision Tree) for their efficiency and robustness to outliers.
    * **Model Training & Evaluation**: Both models were trained and evaluated using Accuracy Score, ROC-AUC Score, and detailed Classification Reports.
    * **Observation**: The **Random Forest Classifier** consistently demonstrated **higher accuracy and better overall metrics** (precision, recall, f1-score) compared to the Decision Tree, which appeared underfitted.
5.  **Inference on Fresh Data**: The trained Random Forest Classifier was then used to predict churn on a separate "fresh" dataset (`churn-bigml-20.csv`).

---

## Conclusion & Results

The **Random Forest Classifier** proved to be the **most effective model** for predicting customer churn in this dataset. It consistently delivered **high accuracy and robust performance** on both testing and unseen "fresh" data, confirming its generalization ability and suitability for real-world deployment where efficiency and accuracy are crucial.

---

## Future Enhancements

* Create an interactive Tableau dashboard for data visualizations.
* Explore deep learning models (e.g., neural networks) for comparative analysis.
* Conduct hyperparameter tuning to further optimize model performance.
