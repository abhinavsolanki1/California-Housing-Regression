# California Housing Price Prediction

## Project Overview
This project explores the California Housing dataset and builds regression models to predict district-level median house values. It covers exploratory data analysis, data quality checks, feature scaling, model evaluation, cross-validation, and hyperparameter tuning.

## Objectives
- Understand the dataset through exploratory data analysis and visualizations.
- Investigate target distribution, feature relationships, correlations, and potential outliers.
- Build a Multiple Linear Regression baseline.
- Compare Linear Regression with Ridge, Lasso, Elastic Net, and Polynomial Regression.
- Evaluate performance using MAE, MSE, RMSE, and R².
- Use cross-validation and hyperparameter tuning to compare models.

## Dataset
The California Housing dataset is loaded using `fetch_california_housing` from scikit-learn. It contains 20,640 observations and eight input features.

The target, `MedHouseVal`, represents median house value in units of $100,000. The target has an upper cap in the dataset, which is an important limitation when interpreting predictions.

## Methodology
1. Dataset inspection and data quality checks
2. Exploratory data analysis and visualizations
3. Feature-target separation and train-test splitting
4. Feature standardization using `StandardScaler`
5. Baseline Multiple Linear Regression
6. Training-set out-of-fold diagnostics
7. Regularized and polynomial regression comparisons
8. Cross-validation and hyperparameter tuning
9. Final evaluation on the held-out test set

## Final Model
Multiple Linear Regression was selected as the final model based on its cross-validation performance and simplicity.

| Test metric | Result |
|---|---:|
| MAE | 0.5332 |
| MSE | 0.5559 |
| RMSE | 0.7456 |
| R² | 0.5758 |

Because the target is measured in units of $100,000, the test MAE is approximately $53,320 and the RMSE is approximately $74,560. These are aggregate error measures, not guarantees for individual predictions.

## Tools and Libraries
- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- Jupyter Notebook

## How to Run
Install the dependencies:

```bash
pip install -r requirements.txt
```

Then open `notebooks/California_Housing_Regression.ipynb` in Jupyter Notebook or VS Code and run the cells in order.

The dataset is loaded through scikit-learn, so internet access may be needed the first time it is downloaded.

## Limitations
- The target values are capped near the upper end of the dataset.
- Linear Regression cannot capture every nonlinear relationship.
- Performance on this dataset may not generalize to other regions or market conditions.

## Author
Abhinav Solanki
