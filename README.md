# Cardiac Function Analysis using CMRI

## Overview:
This project focuses on the analysis of cardiac function, crucial for early disease diagnosis in clinical cardiology. By leveraging cardiac magnetic resonance imaging (CMRI), we classify the images into five diagnostic classes. The end goal is to enhance early disease detection, preventing complications such as heart failure and sudden cardiac arrest.

## Highlights:
- Applied a Random Forest Classifier with hyperparameter tuning (Grid Search CV).
- Achieved an accuracy score of 88.571% with the Random Forest model.
- Implemented Stacking, an ensemble learning technique, to boost the accuracy score to 91.428%.
- Used a voting technique for feature selection to build a robust set of features and avoid overfitting.

## Dataset:
- 150 subjects with MRI images and corresponding partial segmentations and metadata.
- Data split into a training-validation set (100 subjects) and a test set (50 subjects).

## Methodology:
1. **Feature Extraction**:
   - Extracted specific features from the images, such as left ventricle (LV), right ventricle (RV), and myocardium (M) segmentations.
   - Calculated morphological and functional parameters using segmentation functions and feature calculation functions.

2. **Preprocessing**:
   - Splitting, scaling, and verification of class imbalance.
   - Analysis of feature importance.
   - Verification of linear separability and linear relationships between features and target.

3. **Model Development**:
   - Implemented a Random Forest Classifier.
   - Employed Stacking as an additional ensemble learning technique.
   - Hyperparameter tuning using Grid Search CV.

## Results:
- Multiple experiments were conducted with varying feature sets and preprocessing methods.
- Achieved a private score of 91.428% on the Kaggle challenge using the Stacking Classifier with feature selection and robust scaling.

## Conclusion:
Regarding the Random Forest classifier, it was observed that implementing Feature Selection might lead to overfitting, as the average CV score increased but the public and private scores decreased. The model with 16 selected features and scaling, however, showcased the best accuracy on the private subset. The StackingClassifier, despite its high computational cost and processing time, proved to be effective, demonstrating the power of ensemble methods. It's worth noting that the best model as per public scores was found to be overfitted after the release of private scores.

## Feedback and Contributions:
For feedback, queries, or contributions, please raise an issue or create a pull request.

## More Information:
For a deeper dive into the challenge and related details, visit [Kaggle IMA205 Challenge 2023](https://www.kaggle.com/competitions/ima205-challenge-2023).
