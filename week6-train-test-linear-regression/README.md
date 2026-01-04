# Week 6 - Train/Test Split & Linear Regression

This week introduces basic machine learning concepts using scikit-learn.
The goal is to understand the ML workflow by taining a simple linear regression model.

## Goals
- Understand supervised learning
- Learn how to apply train/test split on Jupyter Notebook
- Understand how to train and test Linear Regression models
- Know how to perform model evaluation

## Contents
- week6-train-test-linear-reg.ipynb
- Dataset: Energy Efficiency Dataset

## Methods
- Selected numeric features and defined heating load as the prediction target
- Handled missing values by:
  * Dropping rows with missing target values
  * Imputing missing feature values using the median
- Split data into training (80%) and testing (20%) sets
- Trained a Linear Regression model using scikit-learn
- Evaluated model performance using:
  * R2 score
  * Mean Squared Error (MSE)
- Visualized model performance using an Actual vs Predicted scatter plot

## Results 
- The model achieved a strong R2 score on the test set, indicating it explains a large portion of the variance in heating load.
- Predictions closely follow the actual values, suggesting good generalization to unseen data.
- Based on the visuals, some increased variance is observed at higher heating load values, which is something I learned is expected in linear models.

## Visualization 
- Actual vs Predicted Heating Load:
  A scatter plot comparing predicted heating load values to actual values from      the test set. Points closely to follow a diagonal trend, indicating strong        predictive performance.

## Key Takeaways
- Train/test splitting is important for evaluating real-world model performance
- Linear regression can effectively model relationships between buiilding features and energy efficiency
- Visualizations help identify prediction accuracy and model limitations

## Next Steps 
- Interpret model coefficients to understand feature influence
- Explore additional evaluation plots (residuals)
- Experiment with more complex models to capture non-linear patterns.

## Tools Used 
- Python
- pandas, numpy
- scikit-learn
- matplotlib, seaborn
