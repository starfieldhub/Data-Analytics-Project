1.	Importing Libraries and reading dataset
1.1.	Code Snippet 1: The code imports various essential libraries for data analysis, visualization, and machine learning. It includes modules for oversampling and undersampling techniques, as well as classifiers like Random Forest, Decision Tree, SVM, k-NN, and Logistic Regression. Statistical analysis and model evaluation tools are also imported. Visualization libraries such as Matplotlib, Seaborn, and Plotly are included. Overall, these libraries and modules provide a comprehensive set of tools for data preprocessing, exploration, and model building.
1.2.	Code Snippet 2: INPUT_PATH: Specifies the URL for the dataset in CSV format.
SCALER: Chooses between 'std' for StandardScaler and 'minmax' for MinMaxScaler. SHOW_FIGURE: Controls whether to display figures during execution. FEATURE_SELECTION: Indicates whether feature selection will be applied. APPLY_PCA: Indicates whether Principal Component Analysis (PCA) will be applied. APPLY_OVERSAMPLING: Indicates whether SMOTE Oversampling will be applied. RANDOM_STATE: Sets a fixed random state for reproducibility. Pandas display options are set to show the full content of DataFrame columns and limit floating-point numbers to two decimal places.
1.3.	Code Snippet 3: Reads data and prints the first few lines.

2.	Exploratory Data Analysis:
2.1.	Code Snippet 4: This block provides basic statistics on the dataset, helping to understand the distribution of defaulters and non-defaulters.
2.2.	Code Snippet 5: This visualization helps to understand that this dataset is imbalanced.
 


2.3.	Code Snippet 6: This part of the code checks and prints the data types of each column in the DataFrame. It uses the dtypes attribute of the DataFrame, which provides the data type of each column.
2.4.	Code Snippet 7: This part of the code checks for missing values in the dataset and calculates the total count of missing values, which is 0 in this case.
2.5.	Code Snippet 8: The output of this code snippet will include count, mean, standard deviation, minimum, 25th percentile (first quartile), median (50th percentile or second quartile), 75th percentile (third quartile), and maximum for each numerical column in the dataset.
2.6.	Code Snippet 9: The code generates a correlation heatmap using Seaborn to visualize the relationships between specified numeric columns in the dataset.
 

2.7.	Code Snippet 10: This boxplot visualizes the distribution of values in each selected numerical column. The box represents the interquartile range (IQR), the line inside the box represents the median, and the whiskers extend to the minimum and maximum values within a certain range. Outliers may be identified as points beyond the whiskers. This plot can help in identifying the spread and central tendency of each numerical feature.
 
3.	Data Pre-processing:
3.1.	Code Snippet 11: These operations are typically performed for better readability, consistency, and to prepare the data for analysis.
3.2.	Code Snippet 12, 13, 14: Marriage and Education columns are cleaned, by removing rows with undocumented categories.
3.3.	Code Snippet 15: This code snippet groups the data by education level and default payment status, counts the occurrences, and then visualizes the distribution using a stacked bar plot.
 

3.4.	Code Snippet 16: This code snippet groups the data by marital status and default payment status, counts the occurrences, and then visualizes the distribution using a stacked bar plot.
 

3.5.	Code Snippet 19: This code creates a new dataframe (subset) with selected categorical variables and then plots the count of these variables by the target variable (Default). The categorical variables include 'SEX', 'EDUCATION', 'MARRIAGE', and the payment delay variables ('PAY_1' to 'PAY_6'). The payment delay variables are mapped to their corresponding descriptions for better interpretation in the plots. The plots are organized in a 3x3 grid, displaying the distribution of each variable with respect to the target variable.
 

3.6.	Code Snippet 20: This code converts categorical columns ('SEX', 'EDUCATION', 'MARRIAGE') into one-hot encoded format using pd.get_dummies. The original columns are then dropped, resulting in a DataFrame with one-hot encoded categorical variables.

4.	Splitting Dataset into Training and Test 
4.1.	Code Snippet 23: This code uses train_test_split from scikit-learn to split the dataset into training/validation (X_train_val, y_train_val) and test sets (X_test, y_test). The test_size parameter specifies the proportion of the dataset to include in the test split, and stratify=y ensures that the class distribution is preserved in both sets.
4.2.	Code Snippet 24: This code checks and prints the dimensions and class distribution of the training/validation and test sets. It provides information about the number of samples for each class in both sets.
4.3.	Code Snippet 26: The code performs Principal Component Analysis (PCA) on the training data, prints the explained variance ratios, and plots the explained variance ratio and cumulative explained variance ratio. The number of components is set to the original number of features.
 

5.	Classification Techniques:
5.1.	Code Snippet 29: This code standardizes the features using StandardScaler, fits a logistic regression model on the training set (X_train_val and y_train_val), and then makes predictions on the test set (X_test). The precision score is calculated and printed.
5.2.	Code Snippet 30: This code fits a Random Forest classifier on the training set (X_train_val and y_train_val), makes predictions on the test set (X_test), and calculates the precision score, which is then printed.
5.3.	Code Snippet 31: This code standardizes the features, fits a Support Vector Machines (SVM) classifier on the training set (X_train_val and y_train_val), makes predictions on the scaled test set (X_test_scaled), and calculates the precision score, which is then printed.
5.4.	Code Snippet 32: This code fits a Decision Tree classifier on the training set (X_train_val and y_train_val), makes predictions on the test set (X_test), and calculates the precision score. Optionally, you can uncomment the lines to visualize the Decision Tree.
# Data-Analytics-Project
