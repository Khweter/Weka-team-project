# Credit Card Fraud Detection (WEKA)

This repository contains the files and documentation for our data mining project, where we built a machine learning classification model to detect fraudulent credit card transactions.

## The Problem (Class Imbalance)
When we initially ran the dataset through a standard classifier, we achieved an accuracy of ~89.7%. However, checking the Confusion Matrix revealed that the model detected **0 actual fraud cases**. Because genuine transactions made up the vast majority of the data, the model simply biased towards predicting everything as "genuine".

## Our Approach
To solve the class imbalance issue, we applied the **SMOTE** (Synthetic Minority Over-sampling Technique) filter in WEKA to oversample the minority class (fraud cases) by 800%. 

Once the dataset was balanced, we trained a **J48 Decision Tree** model using 10-fold cross-validation. The tree generated 203 rules to separate genuine transactions from fraudulent ones based on features like distance, velocity, and device type.

## Final Results
After balancing the data, the model successfully identified 5,544 fraud cases. 
Our final evaluation metrics:
- **Accuracy:** 90.77%
- **Precision:** 95.96%
- **Recall (Sensitivity):** 85.43%
- **Specificity:** 96.28%

## Repository Contents
- `Model_before_SMOTE.model`: The initial J48 model trained on raw data (demonstrates the class imbalance issue with 0 actual fraud detection).
- `Model_after_SMOTE.model`: The optimized J48 model after applying the SMOTE filter (successfully detects fraud with high precision).
- `fraud.csv`: The dataset used for training and testing the models.
- `Presentation.pdf`: The presentation slides used for our project defense.

## Team Members
- Youssef Khweter
- Mohamed Mahmoud
- Mohamed Tharwat
- Yassin Mostafa
- Mohamed Essam
- Mona Gehad Anwar
- Mai Mohamed Ibrahim
- Menna Mohamed Gharib
- Nadine Ahmed Abdel-Naby

**Supervised by:** Dr. Ahmed Magdy  
Faculty of AI Engineering, NINU
