# Irrigation Need Prediction — Kaggle Competition

## Problem
Predict irrigation need level (Low/Medium/High) for agricultural fields.

## Dataset
630,000 rows, 19 features, multiclass classification.

## Approach
- EDA: Found severe class imbalance (High: 3.3%), 
  Crop Growth Stage as dominant feature
- Feature Engineering: Moisture_to_Heat_Ratio, 
  Climate_Stress_Index, groupby encoding
- Models: LightGBM, CatBoost, XGBoost, RandomForest
- Validation: StratifiedKFold (5 fold) due to class imbalance

## Results
Public leaderboard score: 0.96023
Best CV score: 0.9849

## Key Learnings
- Crop Growth Stage was the single most predictive feature (30% importance)
- Feature engineering improved CV from 0.9843 to 0.9849
- CV to leaderboard gap persisted suggesting distribution shift
