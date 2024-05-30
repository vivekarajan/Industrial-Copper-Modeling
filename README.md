# Industrial-Copper-Modeling

**Objective**
Enhance your proficiency in data analysis and machine learning with our "Industrial Copper Modeling" project. In the copper industry, dealing with complex sales and pricing data can be challenging. Our solution employs advanced machine learning techniques to address these challenges, offering regression models for precise pricing predictions and lead classification for better customer targeting. You'll also gain experience in data preprocessing, feature engineering, and web application development using Streamlit, equipping you to solve real-world problems in manufacturing.

# Technology used:
- Python
- Numpy
- Pandas
- Scikit-Learn
- Matplotlib
- Seaborn
- Pickle
- Streamlit

#  Installation
To run this project, you need to install the following packages:
pip install numpy
pip install pandas
pip install scikit-learn
pip install matplotlib
pip install seaborn
pip install streamlit

###  Features
  #  Data preprocessing:
  - *Data Understanding*: Before diving into modeling, it's crucial to gain a deep understanding of your dataset. Start by identifying the types of variables within it, distinguishing between continuous and categorical variables, and examining their distributions. In our dataset, there might be some unwanted values in the 'Material_Ref' feature that start with '00000.' These values should be converted to null for better data integrity.
    
  - *Handling null values*: The dataset may contain missing values that need to be addressed. The choice of handling these null values, whether through mean, median, or mode imputation, depends on the nature of the data and the specific feature.
    
  -  Encoding & datatype conversion: To prepare categorical features for modeling, we employ ordinal encoding. This technique transforms categorical values into numerical representations based on their intrinsic nature and their relationship with the target variable. Additionally, it's essential to convert data types to ensure they match the requirements of our modeling process.
    
  -  *Skewness & feature sinding*: Skewness is a common challenge in datasets. Identifying skewness in the data is essential, and appropriate data transformations must be applied to mitigate it. One widely-used method is the log transformation, which is particularly effective in addressing high skewness in continuous variables. This transformation helps achieve a more balanced and normally-distributed dataset, which is often a prerequisite for many machine learning algorithms.
    
  -  *Outliers handling*: Outliers can significantly impact model performance. We tackle outliers in our data by using the Interquartile Range (IQR) method. This method involves identifying data points that fall outside the IQR boundaries and then converting them to values that are more in line with the rest of the data. This step aids in producing a more robust and accurate model.
    
  -  *missing date prediction*: In cases where some delivery dates are precedes the item dates, we resolve this issue by calculating the difference and it's used to train a Random Forest Regressor model, which enables us to predict the corrected delivery date. This approach ensures that our dataset maintains data integrity and accuracy.
    
#  EDA processing:
  - *Skewness Visualization*: To enhance data distribution uniformity, we visualize and correct skewness in continuous variables using **Seaborn's boxplot**. By applying the Log Transformation method, we achieve improved balance and normal distribution, while ensuring data integrity.

  - *Outlier Visualization*: We identify and rectify outliers by leveraging **Seaborn's Boxplot**. This straightforward visualization aids in pinpointing outlier-rich features. Our chosen remedy is the Interquartile Range (IQR) method, which brings outlier data points into alignment with the rest of the dataset, bolstering its resilience.

  - *Feature Improvement*: Our focus is on improving our dataset for more effective modeling. We achieve this by creating new features to gain deeper insights from the data while making the dataset more efficient. Notably, our evaluation, facilitated by **Seaborn's Heatmap**, confirms that no columns exhibit strong correlation, with the highest correlation value at just 0.42 (absolute value), underlining our commitment to data quality and affirming that there's no need to drop any columns.

#  Classification:

- *Won and Lost Classification*: In our predictive journey, we utilize the 'status' variable, defining 'Won' as Success and 'Lost' as Failure. Data points with status values other than 'Won' and 'Lost' are excluded from our dataset to focus on the core classification task.
  
- *Model Accuracy and Metrics*: With the optimized parameters, our Random Forest Classifier achieves an impressive 96.5% accuracy, ensuring robust predictions for unseen data. To further evaluate our model, we leverage key metrics such as the confusion matrix, precision, recall, F1-score, AUC, and ROC curve, providing a comprehensive view of its performance.

- *Algorithm Selection*: After thorough evaluation, two contenders, Decision Tree Classifier and Random Forest Classifier, demonstrate commendable testing accuracy. Upon checking for any overfitting issues in both training and testing, both models exhibit strong performance without overfitting concerns. I choose the Random Forest Classifier for its ability to strike a balance between interpretability and accuracy, ensuring robust performance on unseen data.

#  Regression:
- *Algorithm Selection*: After thorough evaluation, two contenders, the Extra Trees Regressor and Random Forest Regressor, demonstrate commendable testing accuracy. Upon checking for any overfitting issues in both training and testing, both models exhibit strong performance without overfitting concerns. I choose the Random Forest Regressor for its ability to strike a balance between interpretability and accuracy, ensuring robust performance on unseen data.

- *Model Accuracy and Metrics*: With the optimized parameters, our Random Forest Regressor achieves an impressive 95.7% accuracy. This level of accuracy ensures robust predictions for unseen data. We further evaluate our model using essential metrics such as mean absolute error, mean squared error, root mean squared error, and the coefficient of determination (R-squared). These metrics provide a comprehensive assessment of our model's performance.
    
#  project video: https://www.loom.com/share/18c5175562254802b7ad1b2897e76613?sid=09409f4c-67d7-4dfb-95bc-8b11b5c97f48
