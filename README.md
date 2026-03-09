# Kepler Exoplanet Classification

Machine learning project for classifying NASA Kepler objects of interest into:

- `CONFIRMED`
- `CANDIDATE`
- `FALSE POSITIVE`

The repository contains two Jupyter notebooks:

- `Kepler_Exoplanet_EDA.ipynb` for exploratory data analysis
- `Kepler_Exoplanet.ipynb` for preprocessing, training, and evaluation

## Dataset

The project uses the Kepler cumulative dataset stored in `archive (9).zip`.

- Rows: `9,564`
- Columns: `50`
- Target column: `koi_disposition`

Class distribution:

- `FALSE POSITIVE`: `5,023`
- `CONFIRMED`: `2,293`
- `CANDIDATE`: `2,248`

## Workflow

### 1. Exploratory Data Analysis

The EDA notebook examines:

- missing values
- class distribution
- feature relationships such as `koi_kepmag` and `koi_period`
- pairplots and correlation heatmaps for numeric features

### 2. Preprocessing

The training notebook applies:

- label encoding for the target
- median imputation and standard scaling for numeric columns
- most-frequent imputation and one-hot encoding for categorical columns
- train, validation, and test splitting

It also drops `kepler_name` before modeling.

### 3. Modeling

Several models are imported for comparison, including:

- Logistic Regression
- Decision Tree
- Random Forest
- KNN
- XGBoost
- LightGBM

The final notebook fits a `LightGBM` classifier.

## Results

Reported notebook metrics:

- Validation accuracy: `0.9262`
- Test accuracy: `0.9195`
- Final classification report accuracy: `0.8991`
- Macro precision: `0.8621`
- Macro recall: `0.8578`
- Macro F1: `0.8592`

These results show that the model performs well overall, with the strongest performance on the `FALSE POSITIVE` class.

## Project Files

- `README.md`: project overview
- `archive (9).zip`: Kepler dataset
- `Kepler_Exoplanet_EDA.ipynb`: visual analysis and feature exploration
- `Kepler_Exoplanet.ipynb`: preprocessing, training, feature importance, and evaluation

## Run Locally

1. Create and activate a Python environment.
2. Install the required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm jupyter
```

3. Launch Jupyter:

```bash
jupyter notebook
```

4. Open either notebook and run the cells in order.

## Notes

- The notebooks were originally written to run in Google Colab and include a repository clone step.
- For local use, keep `archive (9).zip` in the repository root so the notebook file path continues to work.
