1.	Introduction: The dataset employed in this investigation is sourced from the UCI Machine Learning Repository, specifically the "Default of Credit Card Clients" dataset, accessible at https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients.  It encompasses 30,000 observations, each corresponding to a unique credit card client. These observations are characterized by 24 attributes, providing details on default payments, demographic factors, credit data, payment history, and credit card bill statements of clients in Taiwan spanning the period from April 2005 to September 2005.

The objective of this project is to explore the performance of various classification algorithms on a given dataset, both with and without Principal Component Analysis (PCA). The goal is to evaluate the impact of dimensionality reduction on model performance.

This report outlines the data analysis, preparation, model evaluation, and results.

2.	Data Analyses: Performed a comprehensive analysis of the dataset to gain insights into its structure and characteristics. This included:
a.	Summary statistics of key features.
b.	Visualization of data distribution using histograms, box plots, and correlation matrices.
c.	Identification of any outliers or missing values.

3.	Data Splitting and Preprocessing: The dataset was split into training and testing sets using the train_test_split function. Standardization was applied to scale the features, ensuring that each feature contributes equally to the model. SMOTE (Synthetic Minority Over-sampling Technique) was used to address class imbalance in the training set for the Support Vector Machine algorithm.

4.	Applying Classification Algorithms: Five classification algorithms were considered: Logistic Regression, Random Forest, Naive Bayes, Gradient Boosting, and Support Vector Machine. For each algorithm, a function was created to apply the chosen model, including necessary preprocessing steps. All 5 algorithms were run independently of each other and the Precision, Recall and F1 Score were calculated and displayed. 

5.	PCA Application and Results: PCA was applied to investigate the impact of dimensionality reduction on model performance. The F1 scores for each classification algorithm were compared with and without PCA. Logistic Regression and Naive Bayes maintained similar performance with PCA. Random Forest and Gradient Boosting showed a decrease in F1 scores with PCA. Support Vector Machine exhibited a slight decrease in performance with PCA.

 
 
 



6.	Limitations and Future Improvements:
a.	Limitations: The dataset's specific characteristics may influence the effectiveness of PCA. The choice of classification algorithms and hyperparameter settings may impact results.
b.	Future Improvements: Experiment with different preprocessing techniques. Explore additional classification algorithms and ensemble methods. Fine-tune hyperparameters to optimize model performance. Investigate other dimensionality reduction techniques.

7.	Conclusion: The project provides valuable insights into the performance of classification algorithms with and without PCA. Logistic Regression and Naive Bayes show consistent results, while Random Forest and Gradient Boosting exhibit a decline in performance with PCA. Consideration of the dataset's characteristics and exploration of alternative techniques will be crucial for future improvements. This project serves as a proof of concept, laying the groundwork for further exploration and improvement in the field of classification algorithms.

8.	Code Repository: The complete code for this project is available on GitHub https://github.com/starfieldhub/Data-Analytics-Project/blob/main/CIND820_initial%20code_Yakub.ipynb 

