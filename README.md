# Capstone-Project-ML-Predicting Credit Card Consumption

**Model Documentation: Predicting Credit Card Consumption of Customers**

**Business Objective**:

The primary objective of this project is to develop a predictive model for estimating the credit card consumption of customers for a leading bank. By accurately predicting credit card spending, the bank aims to enhance its customer relationship management, tailor marketing strategies, improve risk management, and optimize credit limits offered to customers.

Methodology:

The analysis and model building process is structured as follows:

1.	**Data Collection and Preprocessing**:
- Data Sources: The project utilizes three datasets: ‘CreditConsumptionData’, ‘CustomerBehaviorData’, and ‘CustomerDemographics’.
- Merging Data: The datasets are merged on the customer ID to form a comprehensive dataset.
- Missing Values: Initially, the dataset had missing values for the ‘cc_cons’ (credit card consumption) variable. A separate DataFrame ‘pred_df’ is created for rows with missing ‘cc_cons’ values for prediction purposes.
- Dropping Insignificant Columns: After merging, redundant columns and missing values not related to the prediction target are dropped.
  
2.	**Exploratory Data Analysis (EDA)**:
- Numerical and Categorical Variables: The analysis starts with the exploration of numerical and categorical variables to understand the data distribution and identify any potential outliers or trends.
  
3.	**Feature Engineering**:
- Creating New Features: Relevant features are created or transformed using RobustScaler for numerical columns and OneHotEncoder for categorical columns to enhance the model's predictive power.

4.	**Model Building**:
- **Splitting Data**: The dataset is split into training and test sets.
- **Model Selection**: Three models are considered: Linear Regression, Decision Tree Regressor, and Random Forest Regressor.
- **Pipeline Creation**: Pipelines are created for each model to streamline the training process and include steps like scaling and fitting the model.
- **Performance Evaluation**: **Root Mean Square Percentage Error (RMSPE)** is used to evaluate the models.

5.	**Model Evaluation**:
- RMSPE Metrics: All three models demonstrated low RMSPE values, indicating good predictive performance. The Random Forest Regressor had the lowest **RMSPE (8.24)**, making it the best choice among the three.

6.	**Prediction**:
- Predicting Missing Values: Using the chosen Random Forest Regressor, predictions are made for the missing ‘cc_cons’ values in ‘pred_df’.

**Modeled Results and Insights**:

•	Model Performance: The Random Forest Regressor outperformed other models with the lowest RMSPE. This implies that the model predictions closely align with actual consumption values.

•	RMSPE Interpretation: An RMSPE close to 0 indicates high predictive accuracy. In this case, the Random Forest model's RMSPE suggests that on average, the predictions deviate by a relatively small percentage from the actual values.

**Recommendations**:

•	**Model Deployment**: The Random Forest model should be deployed for predicting credit card consumption in real-time applications.

•	**Feature Enhancement**: Continually enhance the features by incorporating more customer behavior data and transactional information to further improve model accuracy.

•	**Customer Segmentation**: Use the predictions to segment customers based on their consumption patterns and tailor marketing strategies accordingly.

•	**Risk Management**: Integrate the model predictions into the bank’s risk management framework to better assess credit risk and optimize credit limits.

•	**Continuous Monitoring**: Regularly monitor model performance and retrain with new data to maintain accuracy over time.
