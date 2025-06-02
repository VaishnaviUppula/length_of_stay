# Clinical Claims Length of Stay Prediction

## Project Overview

This project predicts the **length of hospital stay** for patients using clinical claims data. Accurate length-of-stay predictions can help hospitals optimize resource allocation, improve patient care, and reduce costs.

---

## Dataset

The dataset contains clinical claims records with features such as:

- Patient demographics (e.g., gender)
- Admission and discharge dates
- Facility identifiers
- Length of hospital stay (target variable)

---

## Project Structure

1. **Data Cleaning & Preprocessing**  
   - Converted date columns to datetime format  
   - Calculated length of stay from admission and discharge dates  
   - Checked and handled missing or inconsistent values  

2. **Feature Engineering & Data Preparation**  
   - Dropped leaky or identifier columns to avoid data leakage  
   - Extracted year, month, and day from datetime features  
   - Imputed missing numerical values with median and categorical with mode  
   - Encoded categorical variables using label encoding  
   - Applied PCA for dimensionality reduction and noise removal  

3. **Modeling**  
   - Used XGBoost regression model to predict length of stay  
   - Performed hyperparameter tuning with GridSearchCV  
   - Evaluated model performance using RMSE and R² metrics  

---

## Key Results

- **RMSE:** 0.79 (average prediction error less than 1 day)  
- **R²:** 0.88 (model explains 88% of the variance in length of stay)  

These results demonstrate strong predictive performance suitable for practical use in healthcare settings.

---

## How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
2. Prepare your dataset as a CSV file and load it in the notebook or script.

3. Run the preprocessing and feature engineering cells/scripts.

4. Train the model using the modeling script.

5. Use the trained model to predict and evaluate on test data.

## Future Work
1. Incorporate more patient clinical features for improved accuracy

2. Experiment with other models and ensemble techniques

3. Develop a deployment pipeline for real-time predictions in hospital systems
