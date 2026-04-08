# supervised_ml

# Medical Patient Clustering

This project applies unsupervised machine learning techniques to medical data in order to discover hidden patterns among patients without using predefined labels.
The goal is to group patients based on their health indicators such as age, BMI, blood pressure, glucose levels, and more.

## Dataset

The dataset contains medical information for 10,000 patients, including:
Age
Sex
BMI
Blood Pressure (Systolic & Diastolic)
Glucose
Cholesterol
Creatinine

 ##Data Preprocessing

The following steps were performed:
Removed unnecessary columns (e.g., patient_id)
Converted categorical data to numerical format
Handled missing values
Removed or capped outliers
Applied feature scaling (StandardScaler)

## Models Used
1. K-Means
Tested using Elbow Method and Silhouette Score
Result: No clear clusters were found due to high data variability
2. DBSCAN (Final Model)
Used for density-based clustering
Automatically detected clusters and outliers
Tuned parameters (eps and min_samples)

## Results
DBSCAN successfully identified 4 meaningful clusters:
Cluster	Interpretation
0	Healthy individuals
1	Hypertension patients
2	Diabetes patients
3	Diabetes + Hypertension (high-risk)
-1	Outliers / complex medical cases

## Conclusion

This project demonstrates how clustering techniques can be used in healthcare to:
Segment patients
Identify high-risk groups
Support medical decision-making
