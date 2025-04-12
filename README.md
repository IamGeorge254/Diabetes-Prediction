# DIABETES PREDICTION USING MACHINE LEARNING
## Problem Statement

Diabetes is a rapidly growing global health concern, with millions of new cases diagnosed annually. Early detection is critical in preventing complications such as heart disease, kidney failure, and vision loss. Traditional diagnostic methods are often time-consuming, costly, and not always accessible. This project aims to address these challenges by leveraging machine learning techniques for early and accurate diabetes prediction.
## Proposed Solution

We propose a machine learning-based solution that analyzes medical data to predict diabetes risk. The system can efficiently handle large datasets, uncover hidden patterns, and deliver real-time results. Our solution is cost-effective, scalable, and helps healthcare providers make timely decisions, especially in low-resource settings.
## Data Processing Overview

We used a publicly available diabetes dataset containing medical information like glucose levels, BMI, age, and HbA1c_level. The data preprocessing steps included handling missing values, removing duplicates, and normalizing continuous features. Feature selection was carried out to retain the most relevant predictors, ensuring optimal model performance.
## Analytics Insights - Visualizations

Exploratory data analysis revealed significant correlations between glucose level, BMI, and diabetes outcome. A correlation heatmap helped identify redundant features. Histograms showed that higher glucose and BMI values were associated with a greater likelihood of diabetes.
## Data Processing Overview

Outlier Detection and Removal: Applied Z-score analysis to detect outliers (threshold: |Z| > 3) and removed them to improve model reliability.


Data Normalization: Performed Min-Max Scaling to standardize numerical features between 0 and 1, ensuring fair model treatment across all inputs.


Class Imbalance Handling: Used SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset, addressing the underrepresentation of diabetic cases.


Feature Selection: Retained only the most impactful variables based on correlation and feature importance analysis to enhance model performance.
## Model Development Overview

Multiple machine learning models were explored, including Logistic Regression, Decision Tree, Random Forest, and Support Vector Machine (SVM).
Development Workflow:
Train-Test Split: 80% of the data was used for training, 20% for testing.


Cross-Validation: 5-fold cross-validation was implemented to ensure model stability.


Hyperparameter Tuning: Used GridSearchCV for fine-tuning each model's parameters.


Evaluation Metrics: Accuracy, Precision, Recall, F1-score
## Updated Final Model Chosen

After evaluating multiple models, Random Forest Classifier emerged as the best performer due to its robustness, ability to handle feature interactions, and resistance to overfitting.
Final Model Configuration:
Algorithm: Random Forest Classifier


Hyperparameters Used:
n_estimators = 100


max_depth = 10


criterion = 'gini'


random_state = 42


Model Evaluation:
Accuracy: 96.64% (0.9664)


Confusion Matrix:

[[17996   104]
 [  562  1153]]


Classification Report:


Class 0 (Non-Diabetic):


Precision: 0.97


Recall: 0.99


F1-Score: 0.98


Support: 18,100


Class 1 (Diabetic):


Precision: 0.92


Recall: 0.67


F1-Score: 0.78


Support: 1,715


Macro Average:


Precision: 0.94


Recall: 0.83


F1-Score: 0.88


Weighted Average:


Precision: 0.97


Recall: 0.97


F1-Score: 0.96
## Insights

The model performed exceptionally well for the non-diabetic class (Class 0).


There’s a noticeable drop in recall for diabetic cases (Class 1), indicating some diabetic patients were not correctly identified — possibly due to class imbalance or overlapping features.


Despite this, the overall accuracy and precision make the model suitable for real-world application with potential for further tuning.
