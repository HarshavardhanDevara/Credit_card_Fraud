# Credit_card_Fraud
                    Credit Card Fraud Detection 
Introduction:                 
                                   Global economy pays the price of more than $ 24 billion per 
year due to these frauds. Thus, it becomes essential to solve this problem and as a 
result a lot of startups have been born into this \$ 30 billion industry 
                                       Credit Card Frauds are the cases of using someone else's 
credit cards for financial transactions without the information of the card owner. 
Credit Cards were made available in order for the people to increase their buying 
power, It increasing prevalence of credit card fraud in the modern financial landscape 
necessitates robust and efficient detection mechanisms. This case study explores the 
application of AI and ML techniques to develop a Credit Card Fraud Detection 
system, addressing the challenges posed by the growing sophistication of fraudulent 
activities. 
Study Case: 
      credit card fraud is a pervasive issue involving unauthorized use of someone 
else's credit cards, causing substantial financial losses globally. This project aims to 
leverage AI and ML to build automated models for detecting fraudulent transactions 
in the rapidly growing credit card industry. 
Dataset and Attributes: 
Features: The dataset consists of numerical features (V1-V28) resulting from PCA 
transformation, Time (seconds elapsed between transactions), Amount (transaction 
amount), and Class (fraud or non-fraud).  
 Imbalance: The class distribution is highly unbalanced, emphasizing the need for 
specialized techniques to handle skewed data. 
▪ V1 - V28: Numerical features resulting from PCA transformation. 
▪ Time: Seconds elapsed between transactions. 
▪ Amount: Transaction amount. 
▪ Class: Fraud or otherwise (1 or 0). 
 
Approach: 
Data Exploration: Understanding the dataset through statistical analysis, visualization, and 
identifying any patterns or anomalies. 
Feature Selection: Applying statistical tests to select relevant features for modeling. 
Data Balancing: Implementing the Synthetic Minority Over-sampling Technique (SMOTE) to 
address class imbalance. 
Modeling: Implementation and comparison of machine learning models (Logistic 
Regression, SVM, Decision Trees, Random Forest, KNN) to classify credit card transactions as 
fraudulent or genuine. 
Evaluation: Assessing model performance through Cross Validation Score and ROC-AUC 
Score due to the imbalanced nature of the dataset. 
Implementation: 
 Step1: How to read csv data or how to load data. 
▪ Here we are performing ETL pipeline which means to extract Data, Transform 
Data ,    
▪ Load Data. 
▪ We have Raw data which includes null values and duplicate values , so we 
need 
▪ to clean the data and then we will get featured data                    
▪ We have 5 modules to import data and to perform analysis.  
• pandas- mainly used to read data, modify data, Manipulate data. 
• Numpy - used for mathematical purpose like to find mean, 
median,percentile. 
• Matplotlib- base module for visualization purpose.  
• Seaborn – used for Data visualization 
• plotly – used for Data visualization  
Step2: Import all Necessary Libraries: 
• import all the modules 
                 import pandas as pd  
import numpy as np 
                import seaborn as sns  
                import matplotlib.pyplot as plt  
               pd.options.display.float_format = '{:.2f}'.format 
 
read the file: 
• data = pd.read_csv('filepath') 
• r is used to reduce Unicode error. 
• r makes the normal string to raw string to avoid problems with different 
os(Mac/windows) 
 
To check null values by heatmap: 
• sns.heatmap(data.isnull(),cmap = 'magma',cbar = False) 
• if there is less number of null values then we can drop null values. 
Step3: 
Data Visualization 
Target Variable Visualization (Class): 
• The data is clearly highly unbalanced with majority of the transactions 
being No Fraud. 
• Due to highly unbalanced data, the classification model will bias its prediction 
towards the majority class, No Fraud. 
• Hence, data balancing becomes a crucial part in building a robust model. 
Feature Selection 
Correlation Matrix: 
• There are too many features in the dataset and it is difficult to understand 
anything.  
• Hence, we will plot the correlation map only with the target variable  
Data Balancing 
Calculation for Data Balancing : 
• Sampling Strategy : It is a ratio which is the common paramter for 
oversampling and undersampling. 
• Sampling Strategy : ( Samples of Minority Class ) / ( Samples of Majority Class 
) 
Undersampling : Trim down the majority class samples 
• Sampling_Strategy = 0.1 
• 0.1 = ( 492 ) / Majority Class Samples 
Oversampling : Increase the minority class samples 
• Sampling_Strategy = 0.5 
• 0.5 = ( Minority Class Samples ) / 4920 
• For imbalanced datasets, we duplicate the data to deal with the potential 
bias in the predictions. 
• Due to this duplication process, we are using synthetic data for modeling 
purposes to ensure that the predictions are not skewed towards the majority 
target class value. 
Modeling 
1) Logistic Regression  
Model based on Correlation Plot                                                 
Model based on ANOVA Score  
2) Support Vector Classifier  
Model based on Correlation Plot                                                 
3) Decision Tree Classifier : 
Model based on Correlation Plot                                                 
4) Random Forest Classifier : 
Model based on Correlation Plot                                    
Model based on ANOVA Score  
Model based on ANOVA Score 
Model based on ANOVA Score                                                                                                   
5) K-Nearest Neighbors : 
Model based on Correlation Plot                                              
ML Alogrithm Results Table: 
Model based on ANOVA Score                                             
Results Table for models based on Correlation Plot : 
Sr. No ML Algorithm 
1 
Logistic Regression 
Cross Validation Score ROC AUC Score F1 Score (Fraud) 
98.01% 
92.35% 
91% 
2 
Support Vector Classifier 
97.94% 
92.10% 
91% 
3 
Decision Tree Classifier 
96.67% 
91.36% 
90% 
4 
Random Forest Classifier 
97.84% 
91.71% 
91% 
5 
K-Nearest Neighbors 
99.34% 
97.63% 
97% 
Results Table for models based on ANOVA Score : 
Sr. No. ML Algorithm 
1 
Logistic Regression 
Cross Validation Score ROC AUC Score F1 Score (Fraud) 
98.45% 
94.69% 
94% 
2 
Support Vector Classifier 
98.32% 
94.40% 
94% 
3 
Decision Tree Classifier 
97.13% 
93.69% 
93% 
4 
Random Forest Classifier 
98.20% 
94.06% 
94% 
5 
K-Nearest Neighbors 
99.54% 
98.47% 
97% 
Conclusion 
• This is a great dataset to learn about binary classification problem with 
unbalanced data. 
• As the features are disguised, feature selection cannot be assisted based on 
the domain knowledge of the topic. Statistical tests hold the complete 
importance to select features for modeling. 
• Due to the use of SMOTE analysis for balancing the data, the models trained 
on this synthetic data cannot be evaluated using accuracy. Hence, we resort to 
Cross Validation Score and ROC-AUC Score for model evaluation. 
