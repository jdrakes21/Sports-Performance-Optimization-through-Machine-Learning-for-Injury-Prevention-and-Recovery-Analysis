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

A key component of this project is the use of interactive dashboards to evaluate machine learning model performance. Rather than relying solely on static figures, the project incorporates **Plotly-based visualizations** that allow users to explore classifier performance through hover-enabled tooltips and model filtering.

The interactive dashboards support:

- 📊 Hover-enabled Confusion Matrices
- 📈 Interactive ROC Curves
- 📉 Interactive Precision–Recall Curves
- 🔄 Model selection through dropdown filters
- 💾 Exportable HTML dashboards compatible with GitHub Pages

These visualizations provide a more intuitive understanding of model behavior, making it easier to compare classifiers, inspect prediction errors, and evaluate performance across multiple metrics.

> **Interactive dashboards are currently implemented in the `day_approach.ipynb` and `week_approach.ipynb` notebooks.**  
> The `nfl_injury_analysis.ipynb` notebook currently uses static evaluation plots.

---

# 📈 Interactive Visualizations

To enhance model evaluation and interpretability, this project incorporates **interactive Plotly dashboards** for the runner injury prediction models. These dashboards allow users to move beyond static evaluation metrics by exploring classifier performance through hover-enabled visualizations and interactive model filtering.

Interactive dashboards are currently implemented in:

- 🏃 `day_approach.ipynb`
- 🏃 `week_approach.ipynb`

The dashboards include:

- 📊 Interactive Confusion Matrices
- 📈 Receiver Operating Characteristic (ROC) Curves
- 📉 Precision–Recall (PR) Curves
- 🔄 Dropdown filtering to compare individual machine learning models
- 🖱️ Hover tooltips displaying detailed evaluation metrics

> **Note:** The `nfl_injury_analysis.ipynb` notebook currently uses static evaluation plots but may be extended with similar interactive dashboards in future work.

---

# 🔍 Featured Interactive Dashboard

One example of the interactive dashboards included in this project is the **ROC Curve Dashboard**, which compares the performance of all four machine learning models used for day-level injury prediction.

### Dashboard Features

- Compare **KNN**, **Logistic Regression**, **Random Forest**, and **XGBoost** on a single ROC plot.
- Hover over any point to inspect the corresponding **False Positive Rate (FPR)** and **True Positive Rate (TPR)**.
- Filter individual models using the built-in dropdown menu.
- Compare **ROC-AUC** values interactively.
- Zoom and pan to inspect specific regions of the curve.

### Explore the Interactive Dashboard

➡️ **Day Approach ROC Dashboard**

https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_roc_all_models.html

---

# 🚀 Additional Interactive Dashboards

The following interactive dashboards are also available:

| Dashboard | Description |
|-----------|-------------|
| Logistic Regression Confusion Matrix | Hover-enabled confusion matrix displaying prediction outcomes. |
| Day Approach Precision–Recall Dashboard | Interactive comparison of precision and recall across all models. |
| Week Approach ROC Dashboard | ROC comparison for the weekly injury prediction models. |
| Week Approach Precision–Recall Dashboard | Precision–Recall comparison for the weekly injury prediction models. |

### Access the Dashboards

- **Logistic Regression Confusion Matrix**  
  https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/logreg_conf_matrix.html

- **Day Approach Precision–Recall Dashboard**  
  https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/day_pr_all_models.html

- **Week Approach ROC Dashboard**  
  https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_roc_all_models.html

- **Week Approach Precision–Recall Dashboard**  
  https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/week_pr_all_models.html

---

# 🔄 Reproducing the Dashboards

Interactive dashboards are generated automatically by running the final model evaluation cells within the `day_approach.ipynb` and `week_approach.ipynb` notebooks.

The dashboards are exported as standalone HTML files using Plotly, allowing them to be viewed directly in any modern web browser or hosted through GitHub Pages.

---

# 💡 Why Interactive Dashboards?

Traditional evaluation metrics such as accuracy and F1-score provide only summary statistics. The interactive dashboards developed for this project enable a more comprehensive evaluation by allowing users to:

- Compare multiple classifiers simultaneously.
- Explore ROC and Precision–Recall trade-offs interactively.
- Inspect confusion matrix predictions in detail.
- Analyze model behavior across different evaluation metrics.
- Share interactive visualizations without rerunning the notebooks.

These dashboards enhance the interpretability of the machine learning workflow and provide an engaging way to explore model performance.
