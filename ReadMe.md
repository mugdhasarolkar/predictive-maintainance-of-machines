Predictive Maintenance for Industrial Equipment
This project implements machine learning models to predict equipment failure in an industrial setting. Using sensor data such as temperature, torque, and rotational speed, the system aims to identify potential issues before they occur to minimize downtime. 

Project Overview
The core objective is to classify whether a machine will experience a failure (Target) and to identify the specific nature of that failure (Failure Type). The project involves data cleaning, exploratory data analysis (EDA), and the implementation of various classification algorithms. 

Dataset Description
The dataset consists of 10,000 data points with 14 operational features, including: 

Type: Product quality variants: L (Low - 50%), M (Medium - 30%), and H (High - 20%). 

Air temperature [K]: Normalized to a standard deviation of 2 K around 300 K. 

Process temperature [K]: Normalized and added to air temperature plus 10 K. 

Rotational speed [rpm]: Calculated from a power of 2860 W with added noise. 

Torque [Nm]: Normally distributed around 40 Nm. 

Tool wear [min]: Minutes added to the tool during the process based on product type. 

Target: Binary classification (0 = No Failure, 1 = Failure). 

Failure Type: Multi-class labels including Heat Dissipation, Power Failure, Overstrain, and Tool Wear failures. 

Implementation Details
Data Preprocessing:

Dropped non-predictive identifiers like UDI and Product ID. 

Checked for and handled missing or duplicate values. 

Encoded categorical variables (Type and Failure Type) into numeric format using OrdinalEncoder. 

Exploratory Data Analysis:

Visualized feature distributions and correlations. 

Identified that air and process temperatures are highly correlated. 

Modeling:

Split the data into training and testing sets.

Evaluated multiple models: K-Neighbors Classifier, Random Forest Classifier, and Logistic Regression.

Key Results
Best Model: Random Forest Classifier.

Accuracy: Achieved approximately 98% accuracy on the test set.

Insights: The confusion matrix and correlation analysis indicate that failure types are closely related to specific operational targets.

Technologies Used
Language: Python
Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
