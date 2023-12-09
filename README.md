# COMP3125 Individual Project
## Introduction

The exploration and analysis of crime helps us understand and address societal problems; this project uses data science to provide further insight as to the possible patterns in crime. The focal point includes analyzing the very city we live in along with analyzing many popular cities spanning the US.

My objective is to use these patterns in crime to ultimately predict crime and crime rates in the future. Hopefully, this objective will help understand the possible crime and threats of the future. 

[Main Method](https://github.com/yeek1ATWIT/COMP3125_Project/blob/main/codes/Main.ipynb)

## Selection of Data

The model processing and training are conducted using a Jupyter Notebook.

The dataset is called [Crime in Context](https://www.kaggle.com/datasets/marshallproject/crime-rates)[1]. This dataset contains over 40 years of homicide, rape, robbery and assault crimes across 68 police jurisdictions with populations of 250,000 or greater.

Data Preview:

This dataset was modified to exclude any illegal values including blank and NAN values.

## Methods

Tools:
- NumPy: A library used for numerical operations. It additionally handles specially formatted
  arrays, matrices and other mathmatical functions.
- Pandas: A library which offers data structures, manipulation and analysis.
- Difflib (Difference Library): A library used for comparing strings.
- Scikit-learn: A machine learning library which provides analysis and modeling. It includes
  resources like classification, regression and clustering.
- Github: A website allowing for code tracking, sharing and collaboration.
- Jupyter: An interactive Python enviroment.

Inference methods used with Scikit:
- Support Vector Regression (SVR): A complex type of Support Vector Machine (SVM) used for
  finding the best hyperplane with given data.
- Linear Regression: An algorithm which predicts a regression line and assumes a linear
  relationship between the given data.

Inference methods used with difflib:
- get_close_matches: A function which finds the closest matches of a string to a database of
  strings.

Radial Basis Function (RBF) Kernel used with Scikits's SVR:
RBF transforms input data into a higher plane/dimension before developing a regression line. 
It's a technique effectively used when the relationship within the data isn't linear.

Usages:
- NumPy: NumPy was used to handle and manipulate arrays. For example, NumPys were used to
  create the arrays for reporting the predicted crime rate.
- Pandas: Pandas was used to handle and manipulate data; datasets had been modified to
  filter out missing, invalid, or NA values. This was crucial for organizing and cleaning
  the dataset.
- Difflib: Only used to extract suggesting options of any user's queries. For example, If
  a user misspelled a valid city relevant to the dataset, the user would use Difflib to find
  which city/cities that the user meant to type.
- Scikit-learn: Handled the machine learning models which helped calculate and predict most
- queries from the user.

Usage of Linear Regression:
  Linear regression was used to linearly model the relationship between the report year and
  the number of violent crimes in Boston, MA. The model is trained using the historical data
  of boston's violent crimes according to the dataset. Once trained, it was used to predict 
  violent crimes from 2023-2032.
  - Used 'fit' to train the model given data
  - Used 'predict' to extract a predicted output from the model

Efficency of Linear Regression:
  Linear regression was used because it efficently understood the decreasing-slope
  relationship associated with years as the x-axis and violent crimes as the y-axis. Other
  models failed to capture this relationship or failed to capture it efficently.

Assumptions/Limitations with Linear Regression:
- It assumes that the relationships between features of the dataset are linear.
- The developed regression line is sensitive to outliers; the regression assumes that there's
  no outliers in the dataset for Years v. Boston's Violent crimes.
- Due to the downward slope of the regression line, the model assumes that an annual negative violent
  crime rate can be met with enough time. This is impossible because there's no such thing.

Modules Used for Linear Regression:
- Linear Regression class for Sklearn.linear_model

Usage of Support Vector Regression (SVR):
  SVR is used to predict the order of different types of crimes bases on city/state, and it's also used
  to predict the annual rates for each type of violent crime based on a given population number and year.
  Seperate models were not only used for each problem, but for each crime type; Each model instance would
  be assigned and trained with a specific crime type.
  - Used 'fit' to train the model given data
  - Used 'predict' to extract a predicted output from the model
  - Used Kernel 'rbf'
  - Used C
  - Used Gamma

Efficency of Support Vector Regression (SVR):
  SVR captures more complex relationships between features in datasets- usually unachievable with just
  linear relationships. It's used to pursue high means of accuracy with this complex data without 
  significantly compromising speed and memory.

Assumptions/Limitations with Support Vector Regression (SVR):
  - Needs to use a given kernel hyperparameters C and Gamma.
  - SVR is significantly sensitive to these parameters; adjusting these parameters affects its accuracy.

Modules Used for Support Vector Regression (SVR):
- SVR class from sklearn.svm

## Discussion

## Summary

## References
[1] [Crime in Context, 1975-2015](https://www.kaggle.com/datasets/marshallproject/crime-rates)

## Maybe
https://www.kaggle.com/datasets/khanboss/us-crime-dataset
  
