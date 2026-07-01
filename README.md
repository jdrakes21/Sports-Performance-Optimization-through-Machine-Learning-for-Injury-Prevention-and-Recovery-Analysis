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
