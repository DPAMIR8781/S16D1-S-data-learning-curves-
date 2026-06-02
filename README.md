📈 Learning Curves and Polynomial Features Analysis
📌 Project Overview

This project explores how machine learning models learn as the amount of training data increases and how model complexity affects performance.

Using an NBA player dataset, we investigate:

Learning Curves
Cross Validation
Bias vs Variance
Underfitting
Overfitting
Polynomial Features
Model Selection

The goal is to understand how feature engineering and model complexity influence predictive performance.

📊 Dataset

The dataset contains NBA player statistics and a target variable representing player performance.

Features
Feature	Description
poss	Number of possessions
mp	Minutes played
do_ratio	Defense/Offense ratio
pacing	Pace metric
Target
Target	Description
win_rating	Player win rating
🛠 Technologies Used
Python
Pandas
NumPy
Scikit-Learn
Matplotlib
Seaborn
Jupyter Notebook
🔍 Project Steps
1. Cross Validation

A Linear Regression model was trained using only the mp feature.

Cross Validation R² Score

0.5567

Result:

Moderate predictive power
Signs of underfitting
2. Learning Curves

Learning curves were generated to evaluate model performance as training size increased.

Observations:

Training and validation scores converged
No severe overfitting detected
Model performance remained limited
3. Adding Features

Additional features were included:

poss
mp
do_ratio
pacing

Cross Validation R² Score

0.6321

Result:

Performance improved noticeably
Additional features provided useful information
4. Polynomial Features

To capture non-linear relationships, Polynomial Features with degree 2 were introduced.

PolynomialFeatures(degree=2)
Polynomial Model Score
0.8697

Result:

Significant improvement over the linear model
Non-linear patterns were successfully captured
5. Selecting the Best Polynomial Degree

Polynomial degrees from 1 to 10 were evaluated using cross validation.

Degree	CV R² Score
1	0.6321
2	0.8697
3	0.8687
4	0.8540
5	0.8250
6	0.7788
7	0.7234
8	0.6362
9	0.5116
10	0.3242
Best Degree
Degree = 2

Result:

Degree 2 achieved the highest validation score.
Higher degrees caused performance degradation and overfitting.
📉 Mean Squared Error Comparison
Linear Regression
MSE = 4.3606
Polynomial Regression (Degree 2)
MSE = 1.5268

Result:

Polynomial model reduced prediction error significantly.
Better representation of complex relationships in the data.
📈 Key Findings
A simple linear model was insufficient for capturing the relationship between player statistics and win rating.
Adding relevant features improved model performance.
Polynomial Features significantly increased predictive accuracy.
Degree 2 provided the best balance between model complexity and generalization.
Learning curves helped identify bias and variance behavior.
🎯 Conclusion

This project demonstrates the importance of:

Feature Engineering
Learning Curve Analysis
Cross Validation
Model Complexity Control
Polynomial Feature Generation

The final Degree-2 Polynomial Regression model achieved the best overall performance with:

R² = 0.8697
MSE = 1.5268

showing a substantial improvement over the baseline linear regression model.
