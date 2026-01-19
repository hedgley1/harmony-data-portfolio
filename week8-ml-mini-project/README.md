## Overview
This project analyzes a real-world cardiovascular dataset to explore patterns associated with heart disease and build machine learning models for prediction.

## Dataset
- UCI Heart Disease (Cleveland subset)
- Clinical features including age, cholesterol, blood pressure, chest pain type, and other diagnostic indicators
- Target variable: presence of heart disease
  
## EDA
Exploratory data analysis was conducted to understand relationships between clinical features and heart disease. Key variables explored included:
* Age:
  - Created a boxplot using seaborn.boxplot(...) to see the relationship betwwen Age vs Heart Disease. The results showed that patients with heart disease tended to be older on average.
* Cholesterol:
  - Created a boxplot using seaborn.boxplot(...) to see the relationship between Cholesterol vs Heart Disease. The results showed higher typical cholesterol levels were observed among patients with heart disease, through distributions overlapped.
* Chest Pain Type:
  - Created a countplot using sns.countplot(...) to see the relationship between Chest Pain Types vs Heart Disease. The results showed patients in the highest chest pain category appear far more frequently among those with heart disease.

EDA helped guide feature selection and informed expectations for model performance.

## Regression Model
* Linear Regression model was buillt using age as the target variable, to practice continuous prediction and explore relationships between other clinical features (excluding num and heart_disease).
  - Evaluation metrics: Mean Squared Error (MSE) & R<sup>2</sup>
  - Result: The regression model showed a low R<sup>2</sup> value, indicating that age is not strongly predictable from the available clinical measurements.
 
This result highlights the importance of ensuring targets are selected with meaningful predictive relationships and demonstrates that not all modeling tasks yield strong performance, even when implemented correctly.

## Classification Model
* The classification taks focused on predicting heart disease presence as a binary outcome.

* Models used:
  - Logisitc Regression (baseline model)
  - Random Forest Classifier (nonlinear ensemble model)
 
Data preparation included handling missing values, encoding categorical variables, and preventing data leakage.

## Results
* Logistic Regression Accuracy: ~85%
* Random Forest Accuracy: ~88%
Random Forest slightly outperformed Logistic Regression which suggests that nonlinear relationships between clinical features contribute to heart disease prediction. A confusion matrix was used to further evaluate classification performance and error types.

## Key Insights
* Age and chest pain type showed strong associations with heart disease presence.
* Cholesterol appeared to be a contributing risk factor but did not fully separate patients with and without heart disease.
* Logistic Regression provided strong baseline performance, while Random Forest captured additional nonlinear modeling.
* Regression performance reinforced that careful target selection is critical in predictive modeling.

## Limitations & Next Steps
* The dataset is relatively small and limited to a specific patient population.
* Models were evaluated using accuracy and basic metrics without extensive hyperparameter tuning.
* Results are exploratory and not intended for clinical decision-making.

Next steps could include:
* Exploring multiclass classification to predict disease severity.
* Evaluating additional metrics such as precision and recall.
* Examining feature importance in more depth.
* Applying similar methods to larger or more diverse healthcare datasets.
