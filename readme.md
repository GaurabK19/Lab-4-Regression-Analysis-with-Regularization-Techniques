## Overview
This lab explores a series of regression techniques to understand how different models handle prediction tasks using the Diabetes dataset from `sklearn.datasets`. Here I have compared lineared, polynomialized, and regularized regression models and evaluated how each approach predicts disease progression based on various medical attributes.

---

## Purpose of the Lab
The main purpose of this lab is to:
- Build and evaluate different regression models.
- Understand how model complexity affects prediction accuracy.
- Explore how regularization (Ridge and Lasso) helps reduce overfitting.
- Compare model performance using standard evaluation metrics.

---

## Methods and Models Used
The following models were implemented and tested:

1. **Simple Linear Regression**  
   Uses one feature to predict the target variable.

2. **Multiple Regression**  
   Uses all available features to build a more complete linear model.

3. **Polynomial Regression**  
   Introduces polynomial features to capture mild nonlinear patterns.

4. **Ridge Regression**  
   Uses L2 regularization to shrink coefficients and reduce overfitting.

5. **Lasso Regression**  
   Uses L1 regularization to shrink and remove coefficients, performing feature selection.

Each model was evaluated using:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

---

## Key Insights Gained
- **Multiple Regression outperformed Simple Linear Regression**, showing that the Diabetes dataset requires more than one predictor to achieve meaningful accuracy.
- **Polynomial Regression (degree 2)** improved performance slightly, but higher-degree polynomials introduced overfitting.
- **Ridge Regression** provided more stable results by controlling large coefficients without removing features.
- **Lasso Regression** helped simplify the model by eliminating less important predictors, improving interpretability.
- The dataset shows **mostly linear behavior** with minor nonlinear components, making linear and regularized models a good fit.

---

## Challenges and Decisions
- Determining the appropriate polynomial degree required experimentation, as higher degrees quickly caused overfitting.
- Choosing regularization strengths (alpha values) involved balancing bias and variance.
- Visualizing the model results was essential to understanding where certain models performed poorly or overfit the data.
- Some features in the dataset contributed weakly, making feature selection methods like Lasso particularly helpful.

---

## Conclusion
This lab demonstrates how different regression models behave on the same dataset and highlights the importance of balancing model complexity with generalization. Regularization techniques such as Ridge and Lasso provide strong improvements over basic models, especially when the dataset contains predictors with varying levels of importance.