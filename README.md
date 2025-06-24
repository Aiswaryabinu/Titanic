Titanic Dataset Analysis

This project performs an exploratory data analysis and preprocessing of the Titanic dataset.

Overview

The notebook covers the following steps:

1. Loading and Initial Inspection: Reads the Titanic dataset and displays basic information and missing values.
2. Handling Missing Values: Imputes missing values in the 'Age', 'Cabin', and 'Embarked' columns using appropriate strategies (mean for 'Age', mode for 'Cabin' and 'Embarked').
3. Encoding Categorical Features: Applies Label Encoding to the 'Sex' and 'Embarked' columns.
4. Normalization: Scales numerical features ('Age', 'Fare', 'PassengerId', 'Pclass', 'SibSp', 'Parch') using MinMaxScaler.
5. Outlier Detection and Removal: Visualizes outliers using boxplots and removes outliers in numerical columns using the Z-score method with a threshold of 3.
6. Visualization: Compares the distribution of numerical features before and after outlier removal using boxplots.

Dependencies

The project requires the following libraries:

pandas
scikit-learn
matplotlib
seaborn
scipy
numpy

Dataset

The dataset used is the "Titanic-Dataset.csv". It is expected to be in the same directory as the notebook or the path should be updated accordingly.


Overview

1. Loading and Initial Inspection: Reads the Titanic dataset and displays basic information and missing values.
   - Reason: To get a foundational understanding of the dataset's structure, column types, and the extent of missing data before proceeding with analysis or preprocessing.

2. Handling Missing Values: Imputes missing values in the 'Age', 'Cabin', and 'Embarked' columns.
   - Age: Filled with the mean of the 'Age' column.
     - Reason: 'Age' is a numerical variable, and using the mean is a common strategy to fill missing numerical data while preserving the overall distribution as much as possible.
   - Cabin and Embarked: Filled with the mode of their respective columns.
     - Reason: 'Cabin' and 'Embarked' are categorical variables. The mode represents the most frequent category, which is a suitable approach for filling missing values in nominal data.

3. Encoding Categorical Features: Applies Label Encoding to the 'Sex' and 'Embarked' columns.
   - Reason: Machine learning algorithms typically require numerical input. Label Encoding converts categorical labels into numerical form, assigning a unique integer to each category. This is appropriate for nominal data where there is no inherent order between categories.

4. Normalization: Scales numerical features ('Age', 'Fare', 'PassengerId', 'Pclass', 'SibSp', 'Parch') using MinMaxScaler.
   - Reason: Normalization (specifically Min-Max Scaling) transforms features to a specific range (usually 0 to 1). This is important for many machine learning algorithms that are sensitive to the scale of the input features, ensuring that no single feature dominates due to its larger values.

5. Outlier Detection and Removal: Visualizes outliers using boxplots and removes outliers in numerical columns using the Z-score method with a threshold of 3.
   - Reason: Outliers can significantly skew statistical measures and impact the performance of some machine learning models. Boxplots provide a visual way to identify potential outliers. The Z-score method quantifies how far a data point is from the mean in terms of standard deviations. Removing points with a Z-score greater than 3 is a common practice to eliminate extreme values.

6. Visualization: Compares the distribution of numerical features before and after outlier removal using boxplots.
   - Reason: To visually assess the impact of outlier removal on the distribution and spread of the numerical data. This helps confirm whether the outlier removal process was effective.
  

     Exploratory Data Analysis
     
1️⃣ Generated Summary Statistics

    Calculated mean, median, standard deviation, and other descriptive statistics using df.describe() and df.median() on numerical columns like Age, Fare, SibSp, and Parch.
    Ensured statistics were computed after removing outliers for accuracy.     
     
2️⃣ Created Histograms and Boxplots

    Used histograms to visualize the distribution of Age and Fare.
    Plotted boxplots to detect outliers and visualize spread.
    Observed that Fare had high variability and outliers.

3️⃣ Used Correlation Matrix

    Applied df.corr() on numeric columns to find relationships between features.
    Visualized correlations using Seaborn heatmap.
    Found moderate correlation between Fare and Pclass, and weak correlation with survival features.

