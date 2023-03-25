# College Dropout Prediction 

## Overview

Our dataset, found on Kaggle, includes demographic data, social-economic factors and academic performance on students enrolled in undergraduate degrees. 

Our goal is to see if a student’s background has any impact on their academic success in higher education institutions. We will also evaluate the bias of the data set using Aequitas.

Some things to note about our dataset: 
- Data is from students in Brazil in 2021
- Dropouts include students that change major or schools, leading to higher dropout rates compared to students that solely did not continue schooling

## Installing Packages (Jupyter on VSCode)

- %pip install pandas numpy statsmodels matplotlib scikit-learn seaborn --user
- import math

  import pandas as pd
  
  import numpy as np
  
  import statsmodels
  
  import scikit-learn
  
  from sklearn.feature_selection import mutual_info_classif
  
  from sklearn.model_selection import train_test_split
  
  import matplotlib
  
  import matplotlib.pyplot as plt
  
  %matplotlib inline
  
  import seaborn as sns
  
  
- For Aequitas:
  - %pip install aequitas --user
  - from aequitas.group import Group
  
    from aequitas.bias import Bias
    
    from aequitas.fairness import Fairness
    
    import aequitas.plot as ap
    
    from aequitas.preprocessing import preprocess_input_df
    
    from aequitas.plotting import Plot
    

## Challenges

1. While trying to conduct a Linear Regression Analysis we realized that it is not the most ideal model for our data as our target values are binary yes/no values rather than a continuous value. Therefore we proceeded to conduct Logistic Regression which was much more suitable and contributed more to our project goals.

## Conclusion

After running different correlation methods and classifiers, we found that the Curricular units 2nd sem (approved), Curricular units 1st sem (approved), and Curricular units 2nd sem (grade) columns were the most correlation/influential in a students target column variable (dropout or graduate).

After our analysis through Aequitas, we found that when we analyzed the data frame with all protected attributes including “Age at enrollment” then the overall fairness report shows that that the dataset is unfair.

Whereas when we ran an analysis excluding “Age at enrollment” then the overall fairness shows that the dataset is fair and passes all parity test.
For future analysis we would like to broaden the data to higher education institutions in more and define the reason the student is a “dropout” (school change, major change, no longer pursuing degree)


