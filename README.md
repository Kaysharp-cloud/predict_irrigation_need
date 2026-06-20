# Irrigation Need Prediction Model Comparison

This project predicts field irrigation need from soil, weather, crop, and field-management variables. The target has three classes: `Low`, `Medium`, and `High`.

## Models

- Logistic Regression
- Random Forest
- Extra Trees
- LightGBM
- CatBoost

The models are compared using accuracy, macro precision, macro recall, macro F1, and weighted F1. Macro F1 is used as the main ranking metric because the `High` irrigation class is much smaller than the other classes.

## Results

On the current train/test split:

| Model | Accuracy | Macro F1 | Weighted F1 |
| --- | ---: | ---: | ---: |
| CatBoost | 0.9990 | 0.9969 | 0.9990 |
| LightGBM | 0.9950 | 0.9793 | 0.9949 |
| Random Forest | 0.9860 | 0.9276 | 0.9850 |
| Logistic Regression | 0.7830 | 0.6815 | 0.7922 |
| Extra Trees | 0.8390 | 0.5598 | 0.8231 |

Best model: `CatBoost`

## Files

```text
Smart_Irrigation_Need_Prediction.ipynb
data/
  irrigation_prediction.csv
README.md
```

## Dataset

Source: Kaggle dataset `miadul/irrigation-water-requirement-prediction-dataset`

The dataset is included locally at:

```text
data/irrigation_prediction.csv
```

## How to Run

Install the required packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn catboost lightgbm
```

Open and run:

```text
Smart_Irrigation_Need_Prediction.ipynb
```
