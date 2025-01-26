# Cricket Team Final Score Prediction Model

## Model Overview

This machine learning model predicts the **final score of a cricket team** based on real-time match statistics. The model was developed using **historical cricket match data**, and the **Random Forest classifier** demonstrated the best performance after evaluating various machine learning algorithms.

---

## Features and Usage

### **Usage**
To use the model, the user provides match details such as:
- Runs
- Wickets
- Overs played
- Other relevant features

The model outputs the **predicted final score** for the team. A **Flask-based web application** enables real-time predictions during live matches.

### **Input and Output**
- **Input Shape**: A list of features representing the current state of the match (e.g., runs, wickets, overs).
- **Output**: Predicted final score (integer).

---

## System Architecture

### **System Description**
This model is part of a larger web-based system designed for real-time score prediction:
1. The user inputs current match data.
2. The model generates the predicted final score.
3. Outputs are displayed in the Flask web app, providing insights during ongoing cricket matches.

### **Input Requirements**
- Match-related statistics: Runs, wickets, overs, and additional game-specific features.
- User interface: Flask web app for real-time interaction.

### **Downstream Dependencies**
The model operates independently but can be integrated with:
- Match prediction tools.
- Team performance analytics.

---

## Implementation Details

### **Hardware Requirements**
- **Training**: Standard CPU (no GPUs used during training).
- **Inference**: Suitable for real-time use on any mid-tier system.

### **Software Requirements**
- **Python**
- **Scikit-learn**: For the Random Forest implementation.
- **Flask**: For creating the web application.
- **Pickle**: For model serialization.

### **Compute Requirements**
- Training Time: ~30 minutes on a mid-tier CPU.
- Inference Time: <1 second per prediction.

### **Energy Consumption**
- Minimal energy consumption during training and inference.

---

## Model Characteristics

### **Model Initialization**
- Trained from scratch using historical cricket match data.
- No pre-trained models were used.

### **Model Stats**
- **Model Type**: Random Forest
- **Number of Trees**: 100
- **Features Used**: 15
- **Latency**: <1 second for inference

### **Other Details**
- **Pruning/Quantization**: Not applied.
- **Privacy Considerations**: No personal or sensitive data used.

---

## Data Overview

### **Training Data**
- Historical cricket match data containing statistics such as:
  - Runs
  - Wickets
  - Overs played
  - Other match-specific variables
- Data Source: Publicly available cricket databases.

#### **Preprocessing Steps**
1. **Data Cleaning**: Removal of missing values and outliers.
2. **Feature Engineering**: Aggregate match stats such as run rate and average wickets per over.

### **Evaluation Data**
- **Data Split**: 80% training, 10% validation, 10% test.
- **Distribution**: Similar distributions between training and test data.

---

## Evaluation Results

### **Summary**
- The Random Forest model achieved high accuracy in predicting final scores.
- Metrics used:
  - **Mean Squared Error (MSE)**
  - **R-squared (R²)**
- Outperformed other models such as Linear Regression and Decision Trees.

### **Subgroup Evaluation**
- No subgroup analysis performed.
- Future versions could explore:
  - Team-specific performance patterns.
  - Impact of weather conditions on scores.
