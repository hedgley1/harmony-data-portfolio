# Exploring Stroke Risk Factors in Stroke Predictor Dataset

## Overview:
This project explores a Stroke Risk Predictor dataset containing patients' demographics and health information to identify which factors may be associated with increased stroke risk. Stroke is a major global health concern, and understanding risk patterns can support prevention and early detection efforts. Through exploratory data analysis (EDA) and visualization, I examine how variables such as age, gender, BMI, and hypertension relate to stroke outcomes.

## Dataset:
URL: https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

Attributes included: ID, gender, age, hypertension, heart disease, marital status, work type, residence type, average glucose levels, body mass index (BMI), smoking status, and stroke history

Records: 5110
Columns: 12

## Questions:
1. Is stroke prevelance significantly different between genders?
2. How does stroke prevelance vary across different BMI categories?
3. Is the prevelance of stroke higher among people with hypertension compared to those without it?
4. How does stroke prevelance change with age?

## Methods:
1. Data Loading & Inspection:
   * Loaded the dataset and examined its structure, column meanings, and missing values.
   * Identified BMI as the only column with missing data.
2. Data Cleaning:
   * Filled missing BMI values using the median.
   * Created BMI categories (Underweight, Normal, Overweight, Obese) for clearer comparisons.
   * Created Age Bins/Groups (0-20, 21-40, 41-60, 61-80, 80+)
   * Relabeled hypertension into readable categories (0: "No Hypertension", 1: "Hypertension")
   * Removed irrelevant columns that were not used in my analysis (id, ever_married, work_type, Residence_type).
3. Exploratory Data Analysis (EDA);
   * Compared stroke prevalance across gender, BMI categories, hypertension status, and age groups.
4. Visualizations:
   * Created bar charts and percent stacked bar charts to visualize relationships.
   * Compared stroke vs.non-stroke counts within each demographic or health-related group.
     
## Key Findings:
1. Gender vs Stroke:
   * Although there are more females in the dataset, stroke rates between both male and female are extremely similar.
   * Based on this data, it suggests that gender is not a strong predictor in potential stroke risk.
     
2. BMI vs Stroke:
   * Based on the dataset, there is a huge risk of stroke with patients that have a BMI (25 - 29.9), which is considered "Overweight" compared to the other categories.
   * However, the "Obese" category holds the place as second largest risk of strokes for patients. This indicates a correlation between higher BMI's and stroke risk.
   * This suggests that BMI measurements should be closely monitored especially for patients who are considered over the "Normal" range.

3. Hypertension vs Stroke:
   * According to the dataset, patients who have hypertension are at a greater risk of having a stroke compared to patients who do not have hypetension.
   * This closely aligns with medical research that suggests high blood pressure is one of the greatest risk factors for strokes.
  
4. Age Group vs Stroke:
   * Patients who are 80 + (Elderly) have a higher risk factor of gettng a stroke.
   * Additionally, patients who range from 61 - 80 (Older Adult) also have a higher risk of getting a stroke compared to Middle-aged Adult, Young Adult, and Children & Teens.
   * This shows that age should be considered one of the greatest factors or predictors of strokes.
     
## Limitations:
* Correlation, not causation:
  This analysis is exploratory and does not establish cause-and-effect relationships
* Imbalanced dataset:
  Only a small percentage of individuals in the dataset experienced a stroke, which may limit the strength of conclusions.
* Missing clinical detail:
  Important medical factors such as cholesterol, blood pressure levels, family history, diabetes, medication usage, etc. are not included.
* BMI imputation:
  Filling missing BMI values with the median may reduce variability and slightly bias results.
  
## Next Steps:
* Build a predictive model:
  Use logistic regression, decision tree, or RF to predict stroke risk.
* Feature importance analysis:
  Determine which variables contribute most to stoke prediction
* Include more clinical features:
  Enhance the dataset with additional health metrics if available.
* Build interactive visuals:
  Use tools like Plotly or Tableau for richer storytelling.
