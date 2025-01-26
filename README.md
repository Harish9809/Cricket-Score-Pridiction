Cricket Score Predictor

This machine learning model predicts the final score of a cricket team based on real-time match statistics. It utilizes a Random Forest classifier, which demonstrated the best performance after evaluating various machine learning algorithms.

Features and Usage

Features

Input: Real-time match statistics, such as runs, wickets, overs played, and other relevant features.

Output: Predicted final score of the cricket team (integer).

Performance: Quick inference time (<1 second), enabling real-time predictions.

Usage

The user provides current match details, and the model outputs a predicted final score. A Flask-based web application facilitates real-time interaction during live matches.

System Overview

Input Requirements

Match-related statistics, including:

Runs scored

Wickets lost

Overs played

Additional game-specific features

Output

Predicted final score of the batting team.

Real-Time System

The model is integrated into a Flask web application to:

Accept live match data as input

Provide instant score predictions

Display insights and projections during matches

Model Overview

Model Characteristics

Algorithm: Random Forest Classifier

Hyperparameters: Contains 100 decision trees with approximately 15 features.

Training: Built from scratch using historical cricket match data.

Size: Lightweight model suitable for real-time deployment.

Implementation Details

Hardware: Trained on a standard CPU without GPUs.

Software:

Python

Scikit-learn

Flask (web application)

Pickle (model serialization)

Compute Requirements:

Training: Approximately 30 minutes on a mid-tier CPU.

Inference: Under 1 second per prediction.

Energy Consumption: Minimal due to computational efficiency.

Data Overview

Training Data

Source: Publicly available cricket databases with historical match data.

Preprocessing:

Removal of missing values and outliers.

Feature engineering (e.g., run rate, average wickets per over).

Split: 80% training, 10% validation, 10% test.

Evaluation

Metrics:

Mean Squared Error (MSE)

R-squared

Performance:

Outperformed other models like Linear Regression and Decision Trees.

High accuracy in final score prediction.

Known Limitations

Data Dependence: Performance may degrade in scenarios with significant deviations from historical data (e.g., extreme weather, unexpected player injuries).

Lack of Subgroup Analysis: No team- or player-specific evaluations were performed. Future iterations may incorporate these aspects.

Sensitive Use Cases: Designed for entertainment and analysis, not critical decision-making.

Ethical Considerations

Data Privacy: Uses publicly available match data with no sensitive or personal information.

Bias: Continuous monitoring will ensure the model does not unintentionally propagate biases if expanded in the future.

Installation and Usage

Clone the repository:

git clone https://github.com/your-username/cricket-score-predictor.git

Install dependencies:

pip install -r requirements.txt

Run the Flask web app:

python app.py

Access the application at http://localhost:5000 and input match statistics for predictions.

Future Work

Player-Level Analysis: Incorporate player-specific data for more granular predictions.

Weather and Conditions: Adapt the model to account for real-time match conditions, such as weather.

Fairness Analysis: Evaluate fairness if demographic or player-level data is added.
