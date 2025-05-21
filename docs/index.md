Sports Injury Analysis and Prediction

🧠 Project Overview

This project leverages machine learning to forecast and prevent injuries in competitive runners by analyzing training load, recovery, and exertion metrics across both daily and weekly timeframes. The analysis supports evidence-based decisions in training design and athlete monitoring.

Additionally, a comparative study on NFL injuries is included to provide broader context and modeling contrast using a different type of athletic dataset. This analysis combines two datasets and performs multi-class classification to distinguish between injured and non-injured players and identify injury rates for specific body parts.

📊 Project Structure

📁 Notebooks Included:

day_approach.ipynb

-Focuses on daily-level training data for runners.

-Evaluates features such as daily distance, intensity zones, and recovery for injury risk.

-identify short-term load spikes correlated with injury likelihood.

week_approach.ipynb

-Aggregates training metrics at the weekly level.

-Analyzes injury rates across features like total kilometers, tough sessions, Z5-T1-T2 volume, and exertion.

-Produces heatmaps and injury rate breakdowns by grouped feature values.

nfl_injury_analysis.ipynb

-An in-depth exploratory and predictive analysis of NFL player injuries.

-Combines two datasets to create a unified injury profile.

-Performs multi-class classification to predict the type and location of injuries.

-Offers insights into injury rates by body part, player position, and event context.

📈 Interactive Visualizations

Only the day_approach.ipynb and week_approach.ipynb notebooks include interactive graphs with:

-Hover-enabled Plotly and mpld3 charts

-Filterable visualizations by intensity zones, exertion, recovery, etc.

-Grouped injury insights (e.g., by session difficulty or training volume)

Key insight: Athletes with higher tough-session frequency or abrupt training increases are more prone to injuries.

🔍 Embedding Demo Example

This interactive chart shows the injury rate in relation to the number of sessions per week from the day-level dataset:

Hover over each bar to view the injury rate by training session frequency.

Explore additional visualizations by running the notebooks or accessing other HTML files in the docs/ directory.

⚙️ Getting Started

Clone the repository:

git clone https://github.com/jdrakes21/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis.git

Recommended usage order:

day_approach.ipynb

week_approach.ipynb

nfl_injury_analysis.ipynb

Run these notebooks in Jupyter Lab or Google Colab to reproduce results.

🌐 GitHub Pages Documentation

This page is served via GitHub Pages:

https://jdrakes21.github.io/Sports-Performance-Optimization-through-Machine-Learning-for-Injury-Prevention-and-Recovery-Analysis/

It includes detailed writeups, embedded graphs, and model outputs for quick access.

📬 Feedback & Contributions

I welcome community involvement! Contribute by:

Adding new features or metrics

Enhancing model performance

Proposing improvements to visualization or documentation

Open an issue or submit a pull request to get involved.

