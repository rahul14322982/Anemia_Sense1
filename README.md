# Anemia_Sense1

*Anemia prediction web app* — a small machine-learning project to predict presence/absence of anemia from blood/test features.

## Project overview
This repository contains:
- anemia.csv — dataset used for training (raw or preprocessed).
- model.ipynb — the Jupyter notebook where data exploration, preprocessing and model training were performed.
- model.pkl — the exported trained model (recommended to be a pipeline including scaler).
- app.py — Flask web application exposing a HTML form and a JSON endpoint for predictions.
- templates/ — HTML templates for the web UI.
- <p align="center">
  <img src="https://github.com/rahul14322982/Anemia_Sense1/blob/master/OutPut_Screenshort/Screenshot_2-11-2025_182338_127.0.0.1.jpeg" alt="App Screenshot" width="600">
</p> 


## Dataset
Brief description:
- Columns: Age, Gender, Hb, PCV, MCV, MCH, RBC, WBC, Platelets, AnemiaLabel (0 = Not Anemic, 1 = Anemic).
- Source: (add where the data is from; clinical dataset / simulated / Kaggle link, etc).
- Preprocessing:
  - Removed rows with missing critical values.
  - Converted Gender to binary encoding (Male=0, Female=1).
  - Applied scaling (StandardScaler) before model training.

## Modeling
- Tested algorithms: Logistic Regression, Random Forest, XGBoost (optional).
- Final model: RandomForestClassifier inside a sklearn Pipeline with StandardScaler.
- Exported pipeline to model.pkl with joblib.

## Evaluation
- Train/Test split: 80/20 (stratified).
- Metrics reported: Accuracy, Precision, Recall, F1-score, ROC AUC (if available).
- Example results (replace with your actual numbers):
  - Accuracy: 0.92
  - Precision (Anemic): 0.90
  - Recall (Anemic): 0.88
  - ROC AUC: 0.95

## OutPut_Screenshort/ — screenshots of outputs.
- <p align="center">
  <img src="https://github.com/rahul14322982/Anemia_Sense1/blob/master/OutPut_Screenshort/Screenshot_2-11-2025_182338_127.0.0.1.jpeg" alt="App Screenshot" width="600">
</p> 
