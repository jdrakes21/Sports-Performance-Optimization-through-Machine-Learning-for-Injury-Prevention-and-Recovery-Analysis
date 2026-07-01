<h1 align="center">
🏃 Sports Injury Analysis and Prediction
</h1>

<h3 align="center">
Machine Learning Insights for Injury Prevention in Runners and NFL Athletes
</h3>

<p align="center">
Predicting sports injuries through machine learning using physiological workload, recovery, exertion, and athlete performance data.
</p>

<p align="center">
<a href="#-quick-tour">Quick Tour</a> •
<a href="#-getting-started">Getting Started</a> •
<a href="#-repository-structure">Repository Structure</a> •
<a href="#-interactive-visualizations">Visualizations</a> •
<a href="#-results--model-comparison">Results</a> •
<a href="#-documentation">Documentation</a> •
<a href="#-future-work">Future Work</a>
</p>

---

# 🧠 Project Overview

Sports injuries are influenced by a complex interaction of workload, training intensity, recovery, and athlete-specific factors. The goal of this project is to investigate whether machine learning can identify these patterns and accurately predict injury risk before injuries occur.

This repository presents three complementary analyses:

- **Day-Level Runner Analysis** – Predicts injuries using daily training metrics such as running distance, intensity zones, recovery, exertion, and strength training.
- **Week-Level Runner Analysis** – Aggregates athlete workload across weekly intervals to evaluate whether accumulated training load provides stronger predictive power.
- **NFL Injury Classification** – Applies supervised machine learning to classify injury body parts using professional football injury records.

Across these studies, four machine learning algorithms are evaluated:

- K-Nearest Neighbors (KNN)
- Logistic Regression
- Random Forest
- XGBoost

Model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curves
- Precision-Recall Curves
- Interactive Confusion Matrices

Interactive Plotly dashboards were developed to make model evaluation more intuitive through hover-enabled visualizations and model filtering.

---

# 🚀 Quick Tour

Run each notebook directly in Google Colab.

| Notebook | Description | Open |
|-----------|-------------|------|
| Day Approach | Daily runner injury prediction | [Open in Colab](https://colab.research.google.com/drive/128bXRgTRFKK6oewpBnaM2JPeQHisbAaY?authuser=1) |
| Week Approach | Weekly workload injury prediction | [Open in Colab](https://colab.research.google.com/drive/1qRFF-Q0tQWP-o0FT7duoa6M5B4XXQPp1?authuser=1) |
| NFL Injury Analysis | NFL body-part injury classification | [Open in Colab](https://colab.research.google.com/drive/1nFEV6f_hZ2SQYMnSxMVamMbG9tKwxsn4?authuser=1) |

---

# ⚙️ Getting Started

Clone the repository

```bash
git clone https://github.com/jdrakes21/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis.git

cd Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis
```

Install the required packages

```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn matplotlib seaborn plotly mpld3
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

or simply open any notebook directly using the Google Colab links above.

---

# 📂 Repository Structure

```
Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis

│
├── day_approach.ipynb
│      Daily runner injury prediction
│
├── week_approach.ipynb
│      Weekly runner injury prediction
│
├── nfl_injury_analysis.ipynb
│      NFL injury classification
│
├── docs/
│      Interactive HTML dashboards
│
├── datasets/
│      Training datasets
│
├── README.md
│
└── LICENSE
```

---

# 📊 Datasets

## Runner Dataset

The runner dataset contains physiological and workload variables collected from competitive athletes.

Example features include:

- Total kilometers
- Number of training sessions
- Strength training frequency
- Running intensity zones (Z3–4, Z5, T1, T2)
- Recovery score
- Maximum exertion
- Average exertion
- Training success
- Injury occurrence

Two versions of the dataset were analyzed:

- **Daily observations**
- **Weekly aggregated observations**

---

## NFL Dataset

The NFL analysis combines multiple public injury datasets to create a multiclass injury classification problem.

Features include:

- Player position
- Injury event
- Play characteristics
- Injury body part
- Game information

Unlike the runner datasets, which perform **binary injury prediction**, the NFL dataset performs **multiclass injury classification**, predicting the location of an athlete's injury.

---

# 📈 Interactive Visualizations

To enhance model evaluation and interpretability, this project incorporates **interactive Plotly dashboards** for the runner injury prediction models. These dashboards extend beyond traditional static evaluation plots by allowing users to explore classifier performance through hover-enabled visualizations and interactive model filtering.

Interactive dashboards are currently implemented in:

- 🏃 `day_approach.ipynb`
- 🏃 `week_approach.ipynb`

The dashboards include:

- 📊 Interactive Confusion Matrices
- 📈 Receiver Operating Characteristic (ROC) Curves
- 📉 Precision–Recall (PR) Curves
- 🔄 Dropdown filtering to compare machine learning models
- 🖱️ Hover tooltips displaying detailed evaluation metrics

> **Note:** The `nfl_injury_analysis.ipynb` notebook currently uses static evaluation plots. Future work will extend the same interactive dashboard functionality to the NFL injury classification models.

---

# 🔍 Featured Interactive Dashboard

One example of the interactive dashboards included in this project is the **Day Approach ROC Curve Dashboard**, which compares the performance of all four machine learning models used for daily injury prediction.

### Dashboard Features

- Compare **KNN**, **Logistic Regression**, **Random Forest**, and **XGBoost** on a single ROC plot.
- Hover over any point to inspect the corresponding **False Positive Rate (FPR)** and **True Positive Rate (TPR)**.
- Filter individual models using the built-in dropdown menu.
- Compare **ROC-AUC** values interactively.
- Zoom and pan to inspect specific regions of the ROC space.


---

# 📊 Interactive Dashboard Library

## 🏃 Day Approach Dashboards

### Confusion Matrices

- **KNN**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_knn_conf_matrix.html

- **Logistic Regression**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_logreg_conf_matrix.html

- **Random Forest**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_rf_conf_matrix.html

- **XGBoost**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_xgboost_conf_matrix.html

### Model Comparison Dashboards

- **ROC Dashboard**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_roc_all_models.html

- **Precision–Recall Dashboard**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_pr_all_models.html

---

## 🏃 Week Approach Dashboards

### Confusion Matrices

- **KNN**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_knn_conf_matrix.html

- **Logistic Regression**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_logreg_conf_matrix.html

- **Random Forest**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_rf_conf_matrix.html

- **XGBoost**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_xgboost_conf_matrix.html

### Model Comparison Dashboards

- **ROC Dashboard**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_roc_all_models.html

- **Precision–Recall Dashboard**
  - https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_pr_all_models.html

---

# 🚀 Reproducing the Dashboards

Interactive dashboards are generated automatically by running the final model evaluation cells within the `day_approach.ipynb` and `week_approach.ipynb` notebooks.

The dashboards are created using **Plotly** and exported as standalone HTML files, making them viewable in any modern web browser or through GitHub Pages.

Example:

```python
plot_roc_dashboard(
    y_true=y_test,
    prob_dict=probs_day,
    title="Day Approach ROC Curves",
    save_path="docs/day_roc_all_models.html"
)
```

Running the evaluation cells automatically generates all ROC, Precision–Recall, and Confusion Matrix dashboards for the corresponding notebook.

---

# 💡 Why Interactive Dashboards?

Traditional evaluation metrics such as accuracy, precision, recall, and F1-score summarize model performance but do not fully illustrate classifier behavior.

The interactive dashboards developed for this project allow users to:

- Compare multiple machine learning models simultaneously.
- Explore ROC and Precision–Recall trade-offs across different decision thresholds.
- Inspect confusion matrix predictions in detail using hover-enabled tooltips.
- Filter individual models to simplify visual comparisons.
- Share interactive visualizations through GitHub Pages without requiring Python or Jupyter Notebook.

Together, these dashboards provide a richer understanding of model performance and transform the repository from a collection of machine learning notebooks into an interactive and reproducible data science project.

# 📊 Results & Model Comparison

Four machine learning algorithms were evaluated across the runner injury prediction tasks:

- K-Nearest Neighbors (KNN)
- Logistic Regression
- Random Forest
- XGBoost

Model performance was assessed using multiple evaluation metrics, including:

- Accuracy
- Precision
- Recall
- F1-score
- ROC Curves
- Precision–Recall Curves
- Confusion Matrices

Rather than relying on a single metric, models were compared based on their overall ability to correctly identify injured athletes while minimizing false positives and false negatives.

---

# 🏃 Day-Level Injury Prediction

The day-level analysis examined whether injuries could be predicted using information collected from individual training sessions, including training volume, exertion, recovery, and intensity-based running metrics.

### Model Performance Summary

| Model | Accuracy | Overall Assessment |
|--------|----------|-------------------|
| Random Forest | **98%** | Best overall performer |
| KNN | **92%** | Strong baseline with high classification accuracy |
| XGBoost | **87%** | Good predictive performance with nonlinear learning capability |
| Logistic Regression | **61%** | Interpretable baseline but limited by linear decision boundaries |

### Discussion

Random Forest achieved the highest overall performance, demonstrating an excellent balance between precision and recall while accurately distinguishing injured from non-injured athletes. Its ensemble structure enabled the model to capture nonlinear relationships between workload, recovery, and exertion that simpler models were unable to identify.

KNN also performed well after feature scaling but remained sensitive to local neighborhood structure. XGBoost achieved competitive results, although it slightly underperformed Random Forest on this dataset. Logistic Regression provided a useful interpretable baseline but struggled to model the complex interactions present in day-level training data.

---

# 🏃 Week-Level Injury Prediction

The weekly analysis investigated whether aggregating workload over longer periods improved injury prediction performance.

### Model Performance Summary

| Model | Accuracy | Overall Assessment |
|--------|----------|-------------------|
| Random Forest | **99%** | Best overall performer |
| XGBoost | **97%** | Excellent performance |
| KNN | **96%** | Strong predictive capability |
| Logistic Regression | **79%** | Significant improvement over the day-level model but still below ensemble methods |

### Discussion

Aggregating workload across weekly intervals substantially improved predictive performance for every machine learning model. Weekly features better represented cumulative fatigue, recovery trends, and sustained training intensity, enabling the classifiers to identify injury patterns that were less apparent at the daily level.

Random Forest again achieved the highest overall performance, while XGBoost and KNN also demonstrated excellent predictive capability. Logistic Regression improved considerably compared with the day-level analysis but continued to underperform relative to nonlinear ensemble methods.

---

# 🏈 NFL Injury Classification

Unlike the runner analyses, the NFL dataset required multiclass classification to identify the location of an athlete's injury rather than simply predicting whether an injury occurred.

### Model Performance Summary

| Model | Accuracy | Overall Assessment |
|--------|----------|-------------------|
| Random Forest | **66%** | Best multiclass classifier |

### Discussion

The NFL injury classification problem proved substantially more challenging than the runner injury prediction tasks due to the larger number of target classes and pronounced class imbalance.

The Random Forest classifier achieved approximately **66% overall accuracy**, performing particularly well for common injury locations such as ankle and knee injuries while exhibiting lower performance for rare injury classes. These results demonstrate the increased complexity of multiclass injury prediction in professional sports.

---

# 🏆 Overall Model Comparison

| Model | Strengths | Limitations |
|--------|-----------|-------------|
| **Random Forest** | Highest predictive performance, robust to nonlinear relationships, excellent balance of precision and recall | Reduced interpretability compared with linear models |
| **XGBoost** | Strong ensemble learner capable of modeling complex interactions | More computationally intensive and requires additional tuning |
| **KNN** | Simple, intuitive algorithm with competitive performance after feature scaling | Sensitive to feature scaling and neighborhood selection |
| **Logistic Regression** | Fast, interpretable baseline model | Limited ability to capture nonlinear relationships within the data |

---

# 🥇 Best Performing Model

Across both runner injury prediction datasets, **Random Forest consistently achieved the strongest overall performance**, outperforming the remaining classifiers in terms of accuracy and overall classification quality.

The superior performance of Random Forest is likely attributable to its ability to:

- Capture nonlinear relationships between training variables.
- Model complex interactions among workload, recovery, and exertion.
- Reduce overfitting through ensemble averaging.
- Maintain strong predictive performance despite correlated physiological features.

These characteristics make Random Forest particularly well suited for injury prediction problems, where injuries are typically influenced by combinations of training variables rather than isolated metrics.
