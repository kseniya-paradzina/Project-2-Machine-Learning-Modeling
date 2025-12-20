# Project 2 – Machine Learning Modeling and Pipeline (MVP)
## Predicting Flight Status Using Operational, Holiday, and Passenger Traffic Data

This repository contains the Minimum Viable Project (MVP) for Project 2, focused on
building an end-to-end machine learning pipeline to predict flight status outcomes
(On-Time, Delayed, Cancelled) before departure.

The project follows the CRISP-DM methodology and emphasizes reproducibility,
robust preprocessing, and thoughtful interpretation of results.

---

## 📌 Business Problem
Flight delays and cancellations create significant operational and financial challenges
for airlines. Early identification of high-risk flights can support proactive scheduling,
resource allocation, and passenger communication.

The objective of this project is to evaluate whether airline operational data,
augmented with global holidays and passenger traffic information, can be used
to predict flight status outcomes.

---

## 📊 Datasets
This project integrates three datasets:

1. **Airline Operational Dataset**
   - Passenger demographics
   - Airport and route information
   - Flight departure date
   - Target variable: `Flight Status` (On-Time, Delayed, Cancelled)

2. **Global Holidays Dataset (2010–2019)**
   - Public and local holidays by country (ISO3)
   - Used to model seasonal and holiday travel effects

3. **Monthly Passenger Traffic Dataset (2010–2018)**
   - Domestic, international, and total passenger volumes
   - Used to create a seasonal congestion index

All datasets are provided as CSV files and are loaded directly in the notebook.

---

## 🧠 Methodology (CRISP-DM)
The project follows the CRISP-DM lifecycle:

1. **Business Understanding**
   - Define the prediction task and business objectives

2. **Data Understanding**
   - Inspect datasets, schema, and target distribution

3. **Data Preparation**
   - Clean data and handle missing values
   - Engineer holiday and passenger traffic features
   - Merge datasets using robust keys

4. **Modeling**
   - Baseline model: Logistic Regression
   - Advanced model: Random Forest
   - Scikit-learn Pipeline and ColumnTransformer used for reproducibility

5. **Evaluation**
   - Train/test split with stratification
   - Stratified K-Fold cross-validation
   - Classification reports and confusion matrix

---

## ⚙️ Modeling Approach
- **Logistic Regression** was used as a baseline benchmark.
- **Random Forest** was used to capture non-linear interactions.
- Weighted F1-score was used as the primary evaluation metric due to class balance.
- Cross-validation was applied to assess model stability.

---

## 📈 Results Summary
- Both baseline and advanced models achieved weighted F1-scores close to **0.33**.
- Cross-validation results were stable across folds.
- Random Forest did not significantly outperform the baseline model.

These results indicate that the primary limitation lies in the available feature set,
as key operational drivers (e.g., weather, real-time congestion) are not present
in the dataset.

---

## 🔍 Key Insights
- Model complexity alone cannot compensate for limited predictive signal.
- Feature relevance and data quality are critical for meaningful performance gains.
- The pipeline and evaluation strategy are robust and reproducible.

---

## ⚠️ Limitations
- Synthetic dataset with limited real-world signal
- Absence of key operational predictors
- No hyperparameter tuning performed in the MVP stage

---

## 🚀 Next Steps
- Incorporate weather and real-time airport congestion data
- Explore gradient boosting models (XGBoost, LightGBM)
- Perform feature importance and interpretability analysis (SHAP)

---

## 📂 Repository Structure
# Project 2 – Machine Learning Modeling and Pipeline (MVP)
## Predicting Flight Status Using Operational, Holiday, and Passenger Traffic Data

This repository contains the Minimum Viable Project (MVP) for Project 2, focused on
building an end-to-end machine learning pipeline to predict flight status outcomes
(On-Time, Delayed, Cancelled) before departure.

The project follows the CRISP-DM methodology and emphasizes reproducibility,
robust preprocessing, and thoughtful interpretation of results.

---

## 📌 Business Problem
Flight delays and cancellations create significant operational and financial challenges
for airlines. Early identification of high-risk flights can support proactive scheduling,
resource allocation, and passenger communication.

The objective of this project is to evaluate whether airline operational data,
augmented with global holidays and passenger traffic information, can be used
to predict flight status outcomes.

---

## 📊 Datasets
This project integrates three datasets:

1. **Airline Operational Dataset**
   - Passenger demographics
   - Airport and route information
   - Flight departure date
   - Target variable: `Flight Status` (On-Time, Delayed, Cancelled)

2. **Global Holidays Dataset (2010–2019)**
   - Public and local holidays by country (ISO3)
   - Used to model seasonal and holiday travel effects

3. **Monthly Passenger Traffic Dataset (2010–2018)**
   - Domestic, international, and total passenger volumes
   - Used to create a seasonal congestion index

All datasets are provided as CSV files and are loaded directly in the notebook.

---

## 🧠 Methodology (CRISP-DM)
The project follows the CRISP-DM lifecycle:

1. **Business Understanding**
   - Define the prediction task and business objectives

2. **Data Understanding**
   - Inspect datasets, schema, and target distribution

3. **Data Preparation**
   - Clean data and handle missing values
   - Engineer holiday and passenger traffic features
   - Merge datasets using robust keys

4. **Modeling**
   - Baseline model: Logistic Regression
   - Advanced model: Random Forest
   - Scikit-learn Pipeline and ColumnTransformer used for reproducibility

5. **Evaluation**
   - Train/test split with stratification
   - Stratified K-Fold cross-validation
   - Classification reports and confusion matrix

---

## ⚙️ Modeling Approach
- **Logistic Regression** was used as a baseline benchmark.
- **Random Forest** was used to capture non-linear interactions.
- Weighted F1-score was used as the primary evaluation metric due to class balance.
- Cross-validation was applied to assess model stability.

---

## 📈 Results Summary
- Both baseline and advanced models achieved weighted F1-scores close to **0.33**.
- Cross-validation results were stable across folds.
- Random Forest did not significantly outperform the baseline model.

These results indicate that the primary limitation lies in the available feature set,
as key operational drivers (e.g., weather, real-time congestion) are not present
in the dataset.

---

## 🔍 Key Insights
- Model complexity alone cannot compensate for limited predictive signal.
- Feature relevance and data quality are critical for meaningful performance gains.
- The pipeline and evaluation strategy are robust and reproducible.

---

## ⚠️ Limitations
- Synthetic dataset with limited real-world signal
- Absence of key operational predictors
- No hyperparameter tuning performed in the MVP stage

---

## 🚀 Next Steps
- Incorporate weather and real-time airport congestion data
- Explore gradient boosting models (XGBoost, LightGBM)
- Perform feature importance and interpretability analysis (SHAP)

---

## 📂 Repository Structure
```
├── Project2_MVP.ipynb
├── Airline Dataset Updated - v2.csv
├── global_holidays.csv
├── monthly_passengers.csv
└── README.md
```
---

## 🧑‍💻 Author Kseniya Paradzina
This project was completed as part of a data science curriculum focused on
machine learning modeling and reproducible pipelines.
