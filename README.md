# Europe Weather Analysis

## Description

This project explores weather trends across Europe from 2000 to 2009 through detailed exploratory data analysis (EDA), focusing on both monthly and yearly patterns. To represent Europe’s climatic diversity, five cities — Roma, Oslo, Heathrow, Budapest, and Basel — were selected for comparative analysis across key weather parameters. In the final phase, machine learning models were developed to predict daily mean temperature for Heathrow, using a time-aware validation strategy to respect the temporal nature of the data.

## Objectives

- Analyze monthly and yearly weather trends across European cities.
- Select a representative set of cities from diverse regions (north, south, east, west, central).
- Build a regression pipeline to predict **Heathrow's mean daily temperature**.
- Evaluate and compare multiple regression models using time-based cross-validation.
- Interpret performance through R², RMSE and residual plots.

## Technologies & Libraries Used

-  **Languages**: Python
- **Libraries**: pandas, NumPy, matplotlib, seaborn, scikit-learn, statsmodels
- **Modeling Techniques**: Polynomial Regression, Random Forest, Gradient Boosting
- **Validation**: TimeSeriesSplit Cross-Validation

## Project Structure
├── notebooks/ # Jupyter notebooks for EDA, visualization, and modeling
├── README.md # Project overview and documentation
└── .gitignore # Files to ignore in version control

## Dataset citation

Huber, F., van Kuppevelt, D., Steinbach, P., Sauze, C., Liu, Y., & Weel, B. (2022). Weather prediction dataset (Version v5) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7525955

## Results

**Target Variable: Mean Daily Temperature (temp_mean) for Heathrow.**

Models Evaluated:

**-Polynomial Regression**

  -R² (Test): 0.794

  -RMSE (Test): 2.663 °C

**-Random Forest**

 -R² (Test): 0.797

 -RMSE (Test): 2.637 °C

**-Gradient Boosting**

 -R² (Test): 0.801 (highest)

 -RMSE (Test): 2.615 °C (lowest)

Gradient Boosting slightly outperformed the other models in terms of both accuracy (R²) and error (RMSE).

## Conclusion

This project demonstrated that machine learning models, particularly ensemble techniques like Random Forest and Gradient Boosting, can effectively predict daily temperature using weather parameters such as humidity, radiation, and cyclical month encoding. While all models performed reasonably well, Gradient Boosting emerged as the top performer.

The modeling pipeline was built with time-aware data splits to prevent data leakage, and the evaluation metrics confirmed robust generalization to unseen data. Future enhancements could involve more advanced temporal feature engineering (e.g., lag features) and hyperparameter tuning to further boost performance and model explainability.



