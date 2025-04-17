# Earthquake Magnitude Classification and Prediction

This repository presents a comprehensive machine learning framework for predicting and classifying earthquake magnitudes using the SOCR Earthquake Dataset. Our models implement both regression and classification techniques to analyze seismic events and support seismic hazard assessment and forecasting.

## 📌 Overview

This project investigates how various machine learning models can be used to:
- **Predict exact earthquake magnitudes** (Regression)
- **Classify earthquakes into discrete magnitude ranges** (Classification)

Models implemented:
- **Regression**: Random Forest, Neural Network (MLP), LSTM
- **Classification**: Random Forest, Naive Bayes, Support Vector Machine (SVM), Neural Network (MLP)

We also explore:
- Feature importance analysis
- Time series modeling of earthquakes
- Relationship validation with the Gutenberg-Richter law

---

## 📊 Dataset

We use the **[SOCR Earthquake Dataset](http://wiki.stat.ucla.edu/socr/index.php/SOCR_Data_Earthquake_2006)**, which includes:
- Latitude, Longitude
- Depth (km)
- Magnitude (Richter scale)
- Number of seismic stations (NbStations)
- Azimuthal gap (Gap)
- Distance to the nearest station
- Root Mean Square (RMS) error
- Timestamp of events

Synthetic features were also added, including Peak Ground Acceleration (PGA).

---

## 🔧 Preprocessing Steps

- Date formatting and feature extraction
- Standardization of numerical features
- Generation of magnitude classes:
  - **Class 0**: Magnitude < 3.0
  - **Class 1**: 3.0 ≤ Magnitude < 4.5
  - **Class 2**: Magnitude ≥ 4.5
- PGA calculation using Boore-Atkinson attenuation relation

---

## 🚀 Models and Methodology

### 🔢 Regression Models
| Model            | RMSE     | MAE     | R²       |
|------------------|----------|---------|----------|
| Random Forest    | 0.3265   | 0.2353  | 0.411    |
| Neural Network   | 0.3493   | 0.2505  | 0.326    |
| LSTM             | 0.4378   | 0.3226  | 0.004    |

### ✅ Classification Models
| Model            | Accuracy | F1-score | Precision | Recall |
|------------------|----------|----------|-----------|--------|
| Random Forest    | 91.8%    | 89.6%    | 90.1%     | 91.8%  |
| Neural Network   | 91.7%    | 89.3%    | 89.9%     | 91.7%  |
| SVM              | 91.4%    | 88.1%    | 89.5%     | 91.4%  |
| Naive Bayes      | 88.7%    | 87.0%    | 86.0%     | 88.7%  |

---

## 📈 Visualizations

Visuals include:
- Earthquake magnitude distribution
- Spatial mapping of seismic activity
- Timeline of seismic events
- Depth vs. Magnitude correlation
- Predicted vs. actual values (Magnitude and PGA)
- Confusion matrices and classification metrics
- Gutenberg-Richter frequency-magnitude plot

---

## 🧠 Key Findings

- **Depth, Distance, and RMS** are the most significant features for predicting magnitude.
- **Random Forest** consistently outperforms other models in both regression and classification tasks.
- **LSTM** shows promise in time-series prediction but performs worse than ensemble models in static settings.
- Dataset follows the expected **Gutenberg-Richter relationship**, validating its real-world applicability.

---

## 🛠️ Tech Stack

- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- PyTorch / TensorFlow for LSTM model
- Jupyter Notebooks for experimentation
- LaTeX (ACM SIGCONF format) for paper/report generation

---

## 📂 Project Structure

