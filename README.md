# Titanic


This project involves exploring and preprocessing the Titanic Dataset  for potential machine learning modeling. The dataset contains information about passengers aboard the RMS Titanic, including whether they survived. 

    Loaded Dataset : Titanic-Dataset.csv
    Viewed First 5 Rows : Using df.head()
    Checked Data Info : Using df.info()  
        Total of 891 entries 
        12 columns , including both numerical and categorical data
        Mixed data types (int64, float64, object)
         
    Checked Missing Values : Using df.isnull().sum()  
        Age : 177 missing values  
        Cabin : 687 missing values (high number)  
        Embarked : 2 missing values

    Handle missing values in Age, Cabin, and Embarked.
    Encode categorical variables like Sex and Embarked.
    Normalize or scale numerical features.
    Explore data visually using plots.
    Prepare data for machine learning models (classification).
     
