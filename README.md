# Flight-Delay
A machine learning pipeline predicting commercial flight delays in the Indian aviation sector using a Random Forest Regressor model trained on over 500,000 flight records.


#  Commercial Flight Delay Prediction using Machine Learning

[![Paper PDF](https://img.shields.io/badge/Paper-Submitted%20to%20ICAA%202025-blue)](docs/ICAA2025_T12_Flight_Delay_Prediction2.pdf)
[![Python](https://img.shields.io/badge/Python-3.10%2B-green)](#)

##  Project Overview
Flight delays remain a major challenge in the aviation industry, impacting passenger satisfaction and increasing operational costs[cite: 1]. This project focuses on enhancing flight delay prediction specifically within the **Indian aviation sector** using a **Random Forest Regressor** model trained on **524,288 flight records**[cite: 1].

### 👥 Authors 
- **Ishani Ghosh** (Heritage Institute of Technology)[cite: 1]

---

## 📊 Key Results & Model Performance
We evaluated multiple models including Random Forest, Gradient Boosting, and XGBoost[cite: 1]. The **Random Forest Regressor** delivered near-perfect predictive accuracy[cite: 1]:

| Model | Mean Absolute Error (MAE) | Mean Squared Error (MSE) | R² Score |
| :--- | :---: | :---: | :---: |
| **Random Forest Regressor** | **0.1146** | **0.0330** | **0.9996** |
| Gradient Boosting | 4.6749 | 28.6713 | 0.6159 |
| XGBoost | 21.7845 | 140.0837 | -3.6094 |

---

## ⚙️ Methodology & Pipeline
1. **Data Acquisition:** Sourced 524,288 records with features like `ScheduledDeparture`, `ActualDeparture`, `Origin`, `Destination`, and `Airline`[cite: 1].
2. **Preprocessing:** Feature extraction (`ScheduledHour`, `ActualHour`), label encoding for categorical variables, and missing value handling[cite: 1].
3. **Feature Scaling & Splitting:** Applied `StandardScaler` and split data into an 80-20 train-test ratio[cite: 1].
4. **Key Finding:** Feature importance analysis revealed that deviations in actual vs. scheduled departure/arrival times are the strongest predictors of delays[cite: 1].

---

## 📁 Research & Assets
- 📄 [Download Paper (PDF)](docs/ICAA2025_T12_Flight_Delay_Prediction2.pdf)[cite: 1]
- 🖼️ [Download Conference Poster (PPTX)](docs/36x24_poster.pptx)

---

## 🚀 How to Run Locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/ishani008/flight-delay-prediction.git](https://github.com/ishani008/flight-delay-prediction.git)
   cd flight-delay-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook in Jupyter Notebook or VS Code.

////

## 📚 Related & Reference Literature
- 📄 [Predictive Modeling of Aircraft Flight Delay](docs/Kalliguddi_2017_Flight_Delay.pdf) — *Anish M. Kalliguddi & Aera K. Leboulluec (2017)*: Benchmarked Multiple Linear Regression, Decision Trees, and Random Forest on 1M US BTS flight records, demonstrating that Random Forest yields superior predictive accuracy ($R^2 = 0.94$) and identifying late incoming aircraft as the primary delay factor.
