# Titanic Survival Prediction

## Objective: 
Goal of this project is to explore and analyze the factors that influenced the survival of passengers on the Titanic through comprehensive data exploration, build and evaluate machine learning models to predict passenger survival. The models are evaluated both with and without the application of the **Synthetic Minority Over-sampling Technique (SMOTE)** to address class imbalance.

## Dataset:
The dataset used is the well-known Titanic dataset, sourced from the "Titanic - Machine Learning from Disaster" competition on Kaggle. It contains 891 rows and 12 columns, providing various details about the passengers such as age, sex, class, fare, and whether they survived.

## Project Components:
1. **Data Cleansing:**
   - **Duplicated Data Check:** Ensured there were no duplicate records.
   - **Missing Value Treatment:** 
     - Filled missing values in the Age column with the median.
     - Filled missing values in the Embarked column with the mode.
     - Dropped the Cabin column due to a high number of missing values.
   
2. **Exploratory Data Analysis (EDA):**
   - **Univariate Analysis:** Analyzed the distribution of individual features, like Age and Fare.
   - **Bivariate Analysis:** Explored the relationships between survival and other features like age, gender, fare, and class.
   
3. **Data Preprocessing:**
   - **Label Encoding and One Hot Encoding:** Converted categorical variables into numeric formats for model building.
   - **Multicollinearity Handling:** Addressed multicollinearity by calculating the Variance Inflation Factor (VIF) and removing or combining highly correlated variables.
   - **Dataset Splitting:** Split the dataset into training, validation, and test sets.

4. **Model Building:**
   - **Models:**
     - Logistic Regression
     - Random Forest Classifier
     - Extreme Gradient Boosting (XGBoost)
   - **Evaluation Models With and Without SMOTE:**
     - Models were first evaluated on the imbalanced dataset.
     - SMOTE was applied to balance the dataset, and the models were re-evaluated.
   
5. **Finding the Best Model:**
   - The best algorithm for predicting Titanic survival was found to be **Random Forest with SMOTE**. This model achieved high accuracy, with a precision of 0.88 and a recall of 0.85. The high recall indicates that the model is effective at identifying those who survived, making it the most reliable choice for survival prediction.
