README: Disaster Relief Project Part 1
Group Members
Leonce, Emmanuel D (fyb7sx)
Medal, Lionel (djz6nn)
Ontiveros, Victor Alberto (qfw3cr)
Project Title
Disaster Relief Project Part 1

Introduction
In response to the catastrophic earthquake that struck Haiti in 2010, rescue operations faced significant challenges in locating displaced individuals due to damaged infrastructure and communication lines. To address this, high-resolution geo-referenced imagery was collected, highlighting temporary shelters made of blue tarps as indicators of displaced individuals' locations.

The project leverages machine learning and data-mining algorithms to automate the detection of blue tarps in imagery, aiding rescue teams in locating individuals efficiently. This innovative approach aims to enhance the speed and accuracy of disaster relief efforts.

Data Summary
The dataset consists of high-resolution geo-referenced imagery with the following variables:

Class: A categorical variable with five categories (vegetation, soil, rooftop, non-tarp, and blue tarp).
Red, Green, Blue: Numerical variables representing pixel intensity in respective color channels.
Summary Statistics
Variable	Min	1st Qu.	Median	Mean	3rd Qu.	Max
Red	48	80	163	163	255	255
Green	48	78	148	153.7	226	255
Blue	44	63	123	125.1	181	255
Class Distribution
Blue Tarp: 2,022
Rooftop: 9,903
Soil: 20,566
Various Non-Tarp: 4,744
Vegetation: 26,006
Data Visualizations
Histograms: Provide insight into pixel value distributions across color channels.
Scatter Plot Matrix: Highlights strong correlations between the Red, Green, and Blue channels.
Data Preprocessing and Transformation
Handling Missing Values: Rows with NA values were removed.
Converting Class to Binary Outcome: Simplified the task into a binary classification problem.
Normalization: Standardized predictors to improve model performance.
Methodology
Model Training, Tuning, and Validation
Software: Analysis performed in R using:
tidyverse for data manipulation and visualization.
pROC for ROC curve analysis.
GGally for exploratory data analysis.
Validation: Used 10-fold cross-validation to ensure robust performance evaluation.
Metrics for Model Performance Evaluation
Accuracy: Proportion of correctly classified instances.
Precision: Ratio of true positives to predicted positives.
Recall (Sensitivity): Ratio of true positives to actual positives.
F1 Score: Harmonic mean of precision and recall.
ROC-AUC: Area under the ROC curve, indicating overall performance.
Results
Model Performance
Model	Accuracy	ROC-AUC	Recall	Precision	F1 Score
Logistic Regression	0.995	0.998	0.885	0.964	0.923
Linear Discriminant Analysis (LDA)	0.984	0.989	0.801	0.727	0.762
Quadratic Discriminant Analysis (QDA)	0.995	0.998	0.840	0.989	0.907
Threshold Selection
Optimal threshold for all models: 0.5 (based on maximizing Youden's J statistic).

ROC Curves
Logistic Regression & QDA: High AUC (0.998) indicates excellent performance.
LDA: Lower AUC (0.989) but still effective.
Conclusions
1. Best Algorithm
Logistic Regression outperformed LDA and QDA across most metrics in cross-validation:
Accuracy: 99.5%
AUC: 0.998
F1 Score: 0.923
2. Challenges
Poor performance across all models on hold-out data highlighted generalization issues.
Recommendations for improvement:
Hyperparameter tuning.
Exploring ensemble methods like Random Forests or Gradient Boosting.
Data augmentation or feature engineering to enhance model robustness.
3. Real-World Impact
Logistic Regression, with its high sensitivity and specificity, effectively identifies blue tarps in disaster zones. This approach can significantly improve the efficiency of disaster relief operations, ensuring timely aid delivery and saving lives.

Acknowledgments
This project is inspired by the innovative work of the Rochester Institute of Technology, which paved the way for data-driven disaster relief solutions.













