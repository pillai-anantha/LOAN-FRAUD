# Loan-Fraud
# Building models to predict companies that are likely commititng fraud so as to audit them (Python)

# Project1f

## Data Prep:

*Loaded the 2 data files Audit_Risk.csv(776 x 27) and trial.csv(776 x 18)

*Checked for any columns with bad value indiactors(there were none)

*Repalced the null values with median(only 1 value, median because high number of outliers)

*Removed duplicate rows

*Checked for possible keys combination using a recursive function.

*('Sector_score', 'LOCATION_ID', 'PARA_A', 'PARA_B', 'TOTAL', 'numbers', 'Money_Value', 'History', 'Score') is used as key for merginf data sets

*Drop columns with only 1 value, and outliers with threshold of 5 after normalization

*Remove correlated columns(99%) by checking using a correlation map from seaborn

*Created target 'Audit_Risk' and data for building models and used standard scaler

*pairplots and boxplots are created

## Regression models for Audit_Risk:

*Created models using scikit-learn and grid search for hypertuning

*Cross validation used for valuating the models

*Hyperparametrs, test and train scores are stored into 'regression_for_Audit_Risk.csv'

*Visualizations for measured~predicted created

*Linear Regression, Lasso, Ridge, Polynomial, LinearSVC, SVC-linear, SVC-Polynomial, SVC-rbf, SGD, Decision Tree models are built

*Polynomial with degree 2 was the best model with test scores of 0.9924

## Classification models for Risk_x and Risk_y:

*Created models using scikit-learn and grid search for hypertuning

*Cross validation used for valuating models

*Hyperparametrs, test and train scores are stored into 'Classification_for_Risk_of_Audit_Risk_df.csv' and 'Classification_for_Risk_of_trial_df.csv'

*Visualizations for confusion matrix and classification report are created

*KNN, Logistic, SVC-polynomial, SVC-linear, SVC-rbf, LinearSVC and decision tree are created

*Decision Tree was the best model with test scores of 1.00
