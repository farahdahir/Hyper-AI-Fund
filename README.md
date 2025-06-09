# **Customer Interest Prediction for Hyper Artificial Intelligence Fund**
# Overview
This project focuses on building a machine learning model to predict customer interest in a financial product—the Hyper Artificial Intelligence Fund. Using anonymised data from 2,000 customers, several classification algorithms were tested, with the Random Forest model delivering the best performance (82.5% accuracy, 90.8% precision for uninterested customers). The model was designed for real-time CRM integration to help sales teams focus on high-potential leads and reduce customer churn due to irrelevant follow-ups.

# Business Understanding
Hyper Big Bank launched a new investment fund and wanted to optimize their outbound call strategy. Sales representatives speak directly to customers and manually record their interest. This process is time-consuming and inefficient. The business goal was to automate customer classification—identifying those highly likely to show interest (Category 3) and those unlikely to convert (Category 0)—to improve targeting, reduce wasted effort, and personalize communication.

# Data Understanding
The dataset comprised 2,000 anonymised customer records with 18 features (FEAT_0 to FEAT_17) and a categorical target variable (CATEGORY) indicating interest levels:

0: Not interested, do not contact again

1: Low priority

2: Medium priority

3: High interest, high priority

Most features were numeric; two (job title and city) were categorical. One column (FEAT_9) had missing values, and no duplicates were found. Exploratory analysis revealed slight class imbalance and strong correlations among certain variables.

# Modeling and Evaluation
Several classification models were evaluated, including Logistic Regression, Support Vector Machine (SVM), Decision Tree, Random Forest, and XGBoost. After preprocessing (imputation, one-hot encoding, outlier handling, and feature scaling), a Random Forest model achieved the best balance across accuracy, precision, and recall. Key evaluation metrics:

Accuracy: 82.5%

Precision for Category 0: 90.8%

Macro F1-Score: 80.6%

Feature importance analysis showed FEAT_11, FEAT_8, and FEAT_6 contributed most to predictions. Hyperparameters were optimized using grid search with cross-validation.

# Conclusion
The project successfully demonstrated that machine learning can effectively classify customer interest for outbound sales calls. The Random Forest model was selected for its performance and generalization ability. Recommendations include integrating the model into the sales CRM with a real-time dashboard and retraining it periodically with new data. This approach enhances operational efficiency, customer experience, and conversion rates.

----

# Reviewing the Project
The project has 3 files and 2 folders. The `salifort_motors.ipynb` is the main notebook for the project. It is divided into sections alining with the PACE frame-work Plan, Analyse, Construct and Execute. For the Construct stage some code cells are commented out, where the predictive models are fitted to save you time. This does not affect the overral work flow of the project, since the models were fitted and saved as pickle files.

The project also includes an images folder and data folder. Remember all datasets are stored in the data folder along with the pickled models.
