# Titanic-Dataset
Exploratory data analysis and data cleaning on the Titanic dataset using pandas and seaborn.

# Titanic Dataset - Exploratory Data Analysis

Data cleaning, preprocessing, and exploratory data analysis (EDA) on the classic Titanic survival dataset, built in a Jupyter/Colab notebook using `pandas` and `seaborn`.

## Overview

This project walks through a full mini data-analysis pipeline on the Titanic dataset:

1. **Loading & inspection** — reading the CSV and checking structure, types, and summary statistics with `df.info()` and `df.describe()`.
2. **Data cleaning**
   - Dropped irrelevant/unusable columns (`Unnamed: 0`, `deck`).
   - Encoded `sex` as binary (male = 1, female = 0).
   - Filled missing `age` values with the column mean.
   - Removed duplicate rows.
   - Cleaned and imputed missing `embark_town` values using the mode.
   - One-hot encoded categorical columns (`embarked`, `who`, `embark_town`) with `pd.get_dummies`.
   - Mapped `class` (First/Second/Third) to ordinal numeric values.
   - Encoded `alive` as binary (yes = 1, no = 0).
   - Converted remaining boolean columns to 0/1.
   - Exported the cleaned dataset to `Titanic_Cleaned_Final.csv`.
3. **Exploratory Data Analysis** — visualizations built with `seaborn`, including:
   - Count plots for survival, passenger class, sex, siblings/spouses, parents/children, and embarkation point (several segmented by `survived`).
   - Distribution plots (`displot`, `histplot`) for `age` and `fare`.
   - Box plots comparing `age`, `fare`, and `class` against `survived`, `alone`, and `sex`.
   - Scatter and bar plots exploring relationships between `age`, `fare`, and `class`.

## Dataset

The notebook expects a `Titanic.csv` file (the seaborn/Kaggle-style Titanic dataset with columns such as `survived`, `pclass`, `sex`, `age`, `sibsp`, `parch`, `fare`, `embarked`, `class`, `who`, `adult_male`, `deck`, `embark_town`, `alive`, `alone`) in the working directory.

> The raw dataset file is not included in this repo. You can source it from [seaborn's built-in datasets](https://github.com/mwaskom/seaborn-data) or [Kaggle's Titanic competition](https://www.kaggle.com/competitions/titanic/data).

## Requirements

```
pandas
seaborn
matplotlib
```

Install with:

```bash
pip install pandas seaborn matplotlib
```

## Usage

1. Place `Titanic.csv` in the same directory as the notebook (or update the file path in the notebook).
2. Open `Titanic_Dataset.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.
3. Run all cells to reproduce the cleaning steps and visualizations.

## Project Structure

```
.
├── Titanic_Dataset.ipynb   # Main notebook: cleaning + EDA
└── README.md                # Project documentation
```

## Author

Jhanvi Khanna
