# rain-prediction

**Rain Prediction (Binary Classification)**

 <p>&nbsp;</p>

**## Overview**

This project builds a binary classification model to predict rainfall based on historical weather data.
The task is inspired by Kaggle-style datasets and aims to support decision-making in agriculture and outdoor event planning.

 <p>&nbsp;</p>

**## Dataset**

　- Source: Weather dataset (train.csv)

　- Size: ~2,600 records

　- Target: RainToday (Yes/No)

 <p>&nbsp;</p>

**## Preprocessing steps**

　- Dropped ID column

　- Converted Date column to datetime64 type

　- Extracted year, month, day from Date

　- One-hot encoding for categorical features

　- Train/test split (80/20)

 <p>&nbsp;</p>

**## Exploratory Data Analysis**

　- Checked missing values (none found)

　- Histograms of numerical features

　- Inspected categorical features and target distribution

 <p>&nbsp;</p>

**## Models & Methods**

The following models were trained and compared:

**- Decision Tree Classifier**

　- Grid search on max_depth (best at ~10)

　- Used class_weight='balanced' to handle imbalance

**- Random Forest Classifier**

　- Compared performance against Decision Tree

　- Checked feature importance

**- Gradient Boosting Models**

　- XGBoost, LightGBM also applied

　- Hyperparameter tuning using GridSearchCV

 <p>&nbsp;</p>

**## Results**

　- Best Accuracy: ~84%

　- Evaluated false positives vs false negatives

　- Adjusted classification threshold and calibration to improve robustness

 <p>&nbsp;</p>

**## Technologies Used**

　- Python, Pandas, NumPy

　- scikit-learn

　- XGBoost, LightGBM

　- Matplotlib

　- Jupyter Notebook

 <p>&nbsp;</p>

**## Repository Structure**

```

rain-prediction/

├── rain_prediction.ipynb   # Main notebook

├── README.md               # Project description

└── data/                   # Dataset (not included, see below)

```

<p>&nbsp;</p>

**## About Dataset**

The dataset is not included in this repository due to license restrictions. Please download it directly from Kaggle.

https://www.kaggle.com/competitions/mlolympiadbd2024/data

<p>&nbsp;</p>

**## Note**

This notebook was originally developed and executed in a local Jupyter environment. 

Due to the use of custom folder structures (e.g., `data/`, `notebook/`, `model/`), it may not run directly without modifications.  

The main purpose of this repository is to showcase the analysis process and results, rather than to provide a fully reproducible environment.
