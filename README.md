# Machine Efficiency Prediction using Machine Learning

## Overview

This project focuses on predicting the efficiency status of manufacturing machines using Machine Learning techniques. The objective is to classify machine efficiency into three categories:

- Low Efficiency
- Medium Efficiency
- High Efficiency

The project uses operational manufacturing data such as temperature, vibration, production speed, power consumption, network latency, and error rate to analyze machine behavior and predict efficiency levels.

Dataset Source:  
:contentReference[oaicite:0]{index=0}

---

# Problem Statement

Manufacturing industries generate large amounts of operational machine data. Monitoring and predicting machine efficiency helps industries:

- Improve productivity
- Reduce downtime
- Detect inefficient operations
- Optimize maintenance scheduling
- Enhance production quality

This project applies multiple Machine Learning algorithms to classify machine efficiency based on manufacturing sensor and operational data.

---

# Objectives

- Perform Data Cleaning and Preprocessing
- Conduct Exploratory Data Analysis (EDA)
- Train multiple Machine Learning models
- Compare model performance
- Analyze feature importance and correlations
- Visualize model evaluation metrics
- Study the impact of dominant operational features

---

# Dataset Information

The dataset contains manufacturing machine operational records with the following features:

| Feature | Description |
|---|---|
| Timestamp | Time of machine operation |
| Machine_ID | Unique machine identifier |
| Operation_Mode | Active / Idle / Maintenance |
| Temperature_C | Machine temperature |
| Vibration_Hz | Machine vibration frequency |
| Power_Consumption_kW | Power usage |
| Network_Latency_ms | Communication latency |
| Packet_Loss_% | Network packet loss |
| Quality_Control_Defect_Rate_% | Product defect percentage |
| Production_Speed_units_per_hr | Production speed |
| Predictive_Maintenance_Score | Maintenance score |
| Error_Rate_% | Machine error percentage |
| Efficiency_Status | Target variable |

---

# Technologies Used

## Programming Language
- Python

## Libraries & Frameworks
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Tools
- Jupyter Notebook
- VS Code

---

# Project Workflow

## 1. Data Preprocessing

- Converted Timestamp column into datetime format
- Checked null values and data types
- Encoded categorical variables
- Selected important numerical features
- Performed train-test split
- Applied feature scaling using StandardScaler

---

# 2. Exploratory Data Analysis (EDA)

Performed multiple visualizations including:

- Pie Charts
- KDE Plots
- Histograms
- Distribution Plots
- Scatterplots
- Correlation Heatmaps

EDA helped identify:

- Class imbalance in efficiency levels
- Strong negative correlation of Error Rate with efficiency
- Strong influence of Production Speed on machine efficiency

---

# 3. Machine Learning Models Used

The following models were implemented and evaluated:

| Model | Accuracy |
|---|---|
| Linear Regression | 48.61% |
| Logistic Regression | 89.15% |
| Gaussian Naive Bayes | 95.89% |
| Multinomial Naive Bayes | 71.69% |
| Bernoulli Naive Bayes | 77.32% |
| Random Forest Classifier | 100.00% |
| Decision Tree Classifier | 99.99% |
| Support Vector Machine (SVM) | 97.87% |
| K-Nearest Neighbors (KNN) | 92.53% |

---

# Key Findings

- Error Rate (%) showed the strongest negative correlation with machine efficiency.
- Production Speed significantly influenced efficiency prediction.
- Random Forest and Decision Tree achieved extremely high accuracy due to dominant predictive features.
- Cross-validation experiments showed that only two features:
  - Error_Rate_%
  - Production_Speed_units_per_hr

  were capable of predicting efficiency with near-perfect accuracy.

---

# Model Evaluation Metrics

The project uses:

- Accuracy Score
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Cross Validation

---

# Visualizations Included

- Correlation Heatmap
- KDE Distribution Plots
- SVM Decision Boundary
- Confusion Matrices
- Model Accuracy Comparison Graphs
- Moving Average Analysis (SMA, CMA, EMA)

---

# Project Structure

```bash
Machine-Efficiency-Prediction/
│
├── data/
│   └── manufacturing.csv
│
├── notebooks/
│   └── machine_efficiency_prediction.ipynb
│
├── requirements.txt
├── README.md

```

---

# Installation

Clone the repository:

```bash
git clone https://github.com/your-username/machine-efficiency-prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

---

# Future Improvements

- Add XGBoost and LightGBM models
- Deploy using Streamlit or Flask
- Perform feature importance analysis
- Handle class imbalance using SMOTE
- Build real-time predictive maintenance dashboard
- Integrate IoT sensor streaming

---

# Learning Outcomes

Through this project, I learned:

- End-to-end Machine Learning workflow
- Manufacturing data analysis
- Classification model comparison
- Feature correlation analysis
- Cross-validation techniques
- Data visualization and interpretation

---

# License

This project is created for academic and educational purposes.
