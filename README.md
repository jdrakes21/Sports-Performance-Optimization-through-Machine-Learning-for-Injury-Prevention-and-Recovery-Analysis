<h1 align="center">
    Sports Injury Analysis and Prediction
</h1>
<h3 align="center">
 Machine Learning Insights for Runners and NFL Athletes
</h3>
<h3 align="center">
    <a href="#-quick-tour">Quick Tour</a> &bull;
    <a href="#-getting-started">Getting Started</a> &bull;
    <a href="#-notebooks">Notebooks</a> &bull;
    <a href="#-visualizations">Visualizations</a> &bull;
    <a href="#-documentation">Documentation</a> &bull;
    <a href="#-authors">Authors</a> &bull;
    <a href="#-license">License</a>
</h3>

---

This repository contains machine learning workflows to predict and analyze sports injuries, with a focus on competitive runners and NFL players. Models examine training loads, exertion, recovery patterns, and event types to forecast injury risk and localize injury types.

---

## 🚀 Quick Tour

Run the notebooks interactively in Google Colab:

- 🏃‍♂️ **[Day-Level Runner Analysis](https://colab.research.google.com/drive/128bXRgTRFKK6oewpBnaM2JPeQHisbAaY?authuser=1)**
- 🏃‍♂️ **[Week-Level Runner Analysis](https://colab.research.google.com/drive/1qRFF-Q0tQWP-o0FT7duoa6M5B4XXQPp1?authuser=1)**
- 🏈 **[NFL Injury Classification](https://colab.research.google.com/drive/1nFEV6f_hZ2SQYMnSxMVamMbG9tKwxsn4?authuser=1)**

---

## ⚡️ Getting Started

```bash
git clone https://github.com/jdrakes21/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis.git
cd Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis
```

Open the notebooks in Jupyter or Colab and start exploring.

## 📁 Notebooks

- `day_approach.ipynb`: Analyze daily exertion and injury patterns.
- `week_approach.ipynb`: Weekly grouped features and injury rate breakdowns.
- `nfl_injury_analysis.ipynb`: Multi-class injury body-part classifier using merged NFL datasets.

## 📈 Visualizations

### Interactive Plots
All notebooks include hover-enabled Plotly graphs and filtering by session or feature group.


### 📎 Embedding Demos

Interactive graphs are integrated into the `day_approach.ipynb` and `week_approach.ipynb` notebooks using `mpld3`, enabling hover-based insights on injury rates by training features.

To access them:
- Open the `day_approach.ipynb` or `week_approach.ipynb` notebooks in Google Colab or Jupyter Notebook.
- Locate the visualization sections near the end — the code will automatically generate and render interactive charts.
- These include hoverable bars showing injury rate distributions across training loads, recovery, and exertion levels.
- Charts are also saved as `.html` files in the `docs/` folder and can be opened in a browser directly.

Note: The `nfl_injury_analysis.ipynb` notebook uses static plots for classification metrics but can be enhanced with Plotly or mpld3 if desired.

No extra setup is required — just run and interact.


### 🔍 Embedding Demo Example


[Click here to view the interactive injury rate graph by session count](docs/day_approach_nr_sessions.html)

This graph uses `mpld3` to display hoverable tooltips inside the HTML.


## 📖 Documentation

### Table of Contents

- [🏃‍♂️ Day Approach Analysis](#-day-approach-analysis)
  - [Feature Engineering](#feature-engineering)
  - [Injury Classification](#injury-classification)
- [🏃‍♂️ Week Approach Analysis](#-week-approach-analysis)
  - [Grouped Feature Trends](#grouped-feature-trends)
  - [Recovery & Exertion Analysis](#recovery--exertion-analysis)
- [🏈 NFL Injury Modeling](#-nfl-injury-modeling)
  - [Dataset Merging](#dataset-merging)
  - [Multiclass Body Part Classification](#multiclass-body-part-classification)
- [📊 Visualizations](#-visualizations)
  - [Interactive Plots](#interactive-plots)
  - [Embedding Demos](#embedding-demos)
- [🚀 Running in Colab](#-running-in-colab)
- [⚠️ Limitations & Improvements](#️-limitations--improvements)

---

## 🏃‍♂️ Day Approach Analysis

### Feature Engineering
Details about how features like `total kms`, `Z5 zone`, and recovery metrics were engineered from raw input.

### Injury Classification
Binary injury detection based on daily sessions.

---

## 🏃‍♂️ Week Approach Analysis

### Grouped Feature Trends
Breakdown of total kilometers, tough sessions, and injury correlations by quartile or intensity bands.

### Recovery & Exertion Analysis
Evaluation of `avg exertion` and `avg recovery` against injury incidence.

---

## 🏈 NFL Injury Modeling

### Dataset Merging
NFL injury and play data were merged by player and game ID to construct full injury timelines.

### Multiclass Body Part Classification
Prediction of body-part-specific injuries using `RandomForestClassifier`, `XGBoost`, and class balancing techniques.

---

## 🚀 Running in Colab

Each notebook in this project can be launched directly in Google Colab for fast, no-setup experimentation:

- [Day Approach - Colab](https://colab.research.google.com/drive/128bXRgTRFKK6oewpBnaM2JPeQHisbAaY?authuser=1)
- [Week Approach - Colab](https://colab.research.google.com/drive/1qRFF-Q0tQWP-o0FT7duoa6M5B4XXQPp1?authuser=1)
- [NFL Injury Analysis - Colab](https://colab.research.google.com/drive/1nFEV6f_hZ2SQYMnSxMVamMbG9tKwxsn4?authuser=1)

To run locally:

```bash
git clone https://github.com/jdrakes21/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis.git
cd Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis
jupyter notebook
```

---

## ⚠️ Limitations & Improvements

### Known Limitations

- ❌ External variables such as sleep, diet, or psychological stress are not included.
- 📉 Class imbalance (few injuries vs. many non-injuries) may impact model accuracy and generalization.
- 🔄 Week-to-week context may not be fully captured in snapshot-based features.

### Future Improvements

- 🗕 Implement time-series models (LSTM, GRU, Transformers) to capture temporal trends.
- ⚽ Expand to other sports datasets such as soccer or basketball for generalizability.
- 🧠 Use explainable AI (e.g., SHAP, LIME) to interpret feature importance in injury predictions.
- 📈 Build an interactive dashboard (e.g., Streamlit or Dash) for real-time monitoring and decision support.
- 🔍 Integrate athlete profile features such as age, gender, training history, and injury history.

## 👨‍💻 Authors

- **Jervon Drakes** – *ML Model Developer & Analyst*  
GitHub: [@jdrakes21](https://github.com/jdrakes21)

## 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
