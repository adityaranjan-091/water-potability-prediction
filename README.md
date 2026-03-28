# Water Potability Prediction

A machine learning project that predicts whether water is safe for human consumption based on various physicochemical properties.

## Overview

Access to safe drinking water is essential for public health. This project builds and compares classification models to predict water potability (safe = 1 / not safe = 0) using water quality measurements.

## Dataset

The dataset contains **3,276 water samples** with the following features:

| Feature | Description |
|---|---|
| `ph` | pH value of water (0–14) |
| `Hardness` | Capacity of water to precipitate soap (mg/L) |
| `Solids` | Total dissolved solids (ppm) |
| `Chloramines` | Amount of chloramines (ppm) |
| `Sulfate` | Amount of sulfates dissolved (mg/L) |
| `Conductivity` | Electrical conductivity (μS/cm) |
| `Organic_carbon` | Amount of organic carbon (ppm) |
| `Trihalomethanes` | Amount of trihalomethanes (μg/L) |
| `Turbidity` | Measure of light-emitting property of water (NTU) |
| `Potability` | Target — 1 if safe to drink, 0 if not |

Source: [Water Potability Dataset](https://raw.githubusercontent.com/jadanpl/Water-Potability-Prediction/refs/heads/main/water_potability.csv)

## Project Structure

```
Water_Potability_Prediction.ipynb   # Main notebook
README.md
```

## Workflow

1. **Data Loading** — Load the dataset from a public URL
2. **Preprocessing** — Handle missing values using median imputation
3. **Exploratory Data Analysis** — Histograms, pairplots, and correlation heatmap
4. **Model Training** — Train and compare three classifiers:
   - Logistic Regression
   - Random Forest
   - XGBoost
5. **Evaluation** — Accuracy, ROC-AUC score, cross-validation, confusion matrix
6. **Feature Importance** — Identify the most influential water quality features

## Results

| Model | Accuracy | 
|---|---|
| Logistic Regression | ~61% |
| XGBoost | ~65% |
| Random Forest | ~66% |

Random Forest achieved the best overall accuracy.

## Requirements

Install the required Python libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
```

## Usage

Open and run the notebook end-to-end:

```bash
jupyter notebook Water_Potability_Prediction.ipynb
```

## License

This project is open source and available for educational use.
