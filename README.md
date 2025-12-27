# Project 2 – Machine Learning Modeling and Pipeline  
## Predicting Flight Status Using Operational, Holiday, and Passenger Traffic Data

## Project Overview
This project presents an end-to-end machine learning solution developed as part of **Project 2: Machine Learning Modeling and Pipeline**.  
The objective is to predict airline flight status outcomes (**On Time, Delayed, Cancelled**) prior to departure using operational airline data augmented with global holiday information and passenger traffic patterns.

The project emphasizes reproducibility, interpretability, and methodological rigor, following industry best practices and the **CRISP-DM** data science framework.

---

## BLUF (Bottom Line Up Front)
Using a structured CRISP-DM approach, this project demonstrates that while seasonal demand and holiday-related features provide useful contextual signals, accurate early-stage flight disruption prediction is primarily constrained by the availability of granular operational data.  
The final tuned Random Forest model achieved a weighted F1-score of approximately **0.34**, highlighting data limitations rather than modeling deficiencies.

---

## Business Problem
Flight delays and cancellations generate significant operational, financial, and customer experience costs for airlines. These disruptions are often amplified during periods of high demand such as holidays and peak travel seasons.

This project explores whether machine learning models trained on pre-departure operational data—enhanced with holiday timing and passenger traffic indicators—can provide actionable early-warning insights to support proactive airline decision-making.

---

## Data Sources
The analysis integrates three datasets:

- **Airline Dataset**  
  Contains passenger demographics, airport information, route characteristics, pilot identifiers, and flight status labels.

- **Global Holidays Dataset**  
  Provides public holiday information across multiple countries. Holidays are treated as recurring annual events and matched by country, month, and day.

- **Monthly Passenger Traffic Dataset**  
  Includes aggregated domestic and international passenger volumes by country and month, used to construct a seasonal traffic congestion index.

All datasets are included directly in this repository for reproducibility.

---

## Methodology
This project follows the **CRISP-DM** framework:

1. Business Understanding  
2. Data Understanding  
3. Data Preparation & Feature Engineering  
4. Exploratory Data Analysis (EDA)  
5. Modeling & Evaluation  

Key methodological components include:
- Feature engineering for holidays and seasonal passenger congestion
- A reproducible **scikit-learn Pipeline** with `ColumnTransformer`
- Baseline and advanced classification models
- Stratified cross-validation and hyperparameter tuning
- Transparent interpretation of model limitations

---

## Modeling Approach
The following models were evaluated:

- **Baseline Model:** Logistic Regression  
- **Advanced Model:** Random Forest Classifier  

Model evaluation was performed using **weighted F1-score**, appropriate for multi-class classification with balanced class distributions.  
Hyperparameter tuning was conducted using `GridSearchCV`, and the final tuned Random Forest pipeline was selected as the final model.

The trained pipeline was serialized for reproducibility.

---

## Key Results
- Best cross-validated weighted F1-score: **~0.34**
- Performance improvements from model tuning were modest
- Results indicate that predictive performance is primarily constrained by feature signal strength rather than algorithm complexity

---

## 📂 Repository Structure
```
Project-2-Machine-Learning-Modeling/
│
├── .gitignore
├── Airline Dataset Updated - v2.csv
├── Project_2_CRISP_DM_Flight_Status_Model.ipynb
├── README.md
├── final_random_forest_pipeline.joblib
├── global_holidays.csv
└── monthly_passengers.csv
```
---

## 🧑‍💻 Author Kseniya Paradzina
This project was completed as part of a data science curriculum focused on
machine learning modeling and reproducible pipelines
