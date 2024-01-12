# Multiclass-Prediction-of-Cirrhosis-Outcome

This project aims to predict the health status of applicants as censored (C) indicating the patient was alive at N days, (CL) indicating the patient was alive at N days due to liver transplant, or (D) indicating that the patient was deceased at N days, using features like platelets, drugs, amount of minerals intake etc.

Data
The data consists of a training set train_folds.csv with the patient health details and the Health Status split into five folds. There is also a test set test.csv with similar features minus the  Health Status to be predicted.

Preprocessing
The features are preprocessed by 2 methods to test the performance of various feature engineering methods:

1. Log transforming numerical features
2. Standardization
   
Encoding categorical features using LabelEncoder
Scaling numerical features using StandardScaler
Model
An XGBoost Classifier model is trained on the training folds in a stratified manner, and predictions are made on the test set by averaging predictions from each fold model.

Evaluation
Model performance is evaluated using log loss between predicted probabilities and actual health status for each fold.

Results
The model achieves a log loss of ~0.49 on the validation sets. The final predictions are saved in submission.csv.

Contact
For any questions, please reach out to khandelwallokesh@iitgn.ac.in


