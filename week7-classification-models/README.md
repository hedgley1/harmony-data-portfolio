# Week 7 - Classification Models (Titanic)

This week I practiced classification models using the Titanic dataset. The goal is to predict whether a passenger survived based on demographic and travel-related features. Two models were traind and compared: Logistic Regression and Random Forest.

## Dataset
- Titanic: machine Learning from Disaster (Kaggle)
- Target: 'Survived' (0 = did not survive, 1 = survived)

## Data Preparation
- Dropped columns with high missing values or low predictive values: 'Cabin', 'Name', 'Ticket', 'PassengerId'
- Filled missing values:
  * 'Age' -> median
  * 'Embarked' -> mode
- One-hot encoded categorical variables: 'Sex', 'Embarked'
- Train/test split: 80/20 with a fixed random_state

## Models Trained
1. **Logistic Regression**
2. **Random Forest Classifier**

## Results 
- Logistic Regression Accuracy: **68.2%**
- Random Forest Accuracy: **73.7%**

Random forest performed better, likely because Titanic survival depends on nonlinear feature interactions that tree-based ensemble models capture more effectively than linear models.

## Visualization
A confusion matrix was used to evaluate the Random Forest classifier's performance by showing the number of correct and incorrect predictions for each class. This visualization helps highlight how the model distinguishes between survivors and non-survivors and provides insight beyond overall accuracy.

## Next Steps
- Evaluate beyond accuracy (confusion matrix, precision, recall)
- Tune random forest hyperparameters (e.g., max_depth, min_samples_split)
- Explore feature importance to understand which varaibles most influenced survival predictions.
