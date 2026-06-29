<h4> Heart Disease Prediction Using Machine Learning </h4>
This project focuses on predicting the presence of heart disease using machine learning and deep learning methods. Cardiovascular diseases remain one of the leading causes of death worldwide, and early diagnosis plays an important role in prevention and treatment. The aim of this project was to develop and compare classification models capable of identifying patients with heart disease based on clinical features.The project included exploratory data analysis, data preprocessing, model training, hyperparameter tuning, model evaluation, and feature importance analysis.

<h4> Dataset </h4>
The analysis was based on the Heart Disease Cleveland dataset from the UCI Machine Learning Repository, also available through Kaggle. The dataset contains clinical data from 303 patients and includes 14 variables describing patients’ health status.
The target variable indicates whether heart disease is present:

1 — presence of heart disease

0 — absence of heart disease

Selected features used in the analysis included:

age — patient age

sex — patient sex

cp — chest pain type

trestbps — resting blood pressure

chol — serum cholesterol level

thalach — maximum heart rate achieved during exercise

oldpeak — ST depression induced by exercise

ca — number of major vessels visible in fluoroscopy

thal — thallium stress test result

<h4> Models </h4>
Several machine learning and deep learning models were compared:

Logistic Regression

Decision Tree

Support Vector Machine

Multi-Layer Perceptron

Random Forest

Gradient Boosting

HeartNet BN

HeartNet Residual

The deep learning models were implemented using PyTorch. HeartNet BN used Batch Normalization and Dropout, while HeartNet Residual included residual connections.

<h4> Evaluation Metrics </h4>
The models were evaluated using the following metrics:

Accuracy

Precision

Recall

F1-score

ROC-AUC

Confusion Matrix

Cross-validation ROC-AUC

Since this is a medical classification problem, Recall was especially important because false negative predictions may correspond to patients with heart disease incorrectly classified as healthy.

<h4> Results </h4>
The best overall performance was achieved by the HeartNet BN model, which obtained:
Accuracy: 0.933
Precision: 1.000
Recall: 0.857
F1-score: 0.923
ROC-AUC: 0.967

The second-best model was HeartNet Residual, which achieved a ROC-AUC of 0.963. Among classical machine learning models, the best performance was obtained by the tuned Random Forest model, with a ROC-AUC of 0.956.

Logistic Regression also performed very well, reaching:
Accuracy: 0.917
F1-score: 0.902
ROC-AUC: 0.953

This result is particularly interesting because a relatively simple and interpretable linear model achieved performance close to more complex deep learning architectures.

<h4> Feature Importance </h4>
Feature importance analysis showed that the most informative predictors of heart disease were: thal, ca, cp, thalach, oldpeak, exang.
The consistency of feature importance results across different models suggests that these variables are strongly associated with the risk of heart disease in the analyzed dataset.

<h4> Conclusions </h4>
The results show that deep learning models achieved the highest predictive performance, especially the HeartNet BN architecture. However, the advantage over the best classical machine learning models was relatively small. Logistic Regression and Random Forest also achieved strong results while offering better interpretability. This suggests that, for this dataset, the relationships between clinical variables and heart disease can be effectively captured both by classical machine learning methods and by carefully designed neural network architectures.
