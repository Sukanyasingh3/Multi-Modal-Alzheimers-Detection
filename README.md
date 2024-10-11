# Alzheimer's Disease Diagnosis Using Multi-modal Learning

This project develops a multimodal model to assess Alzheimer's disease using numerical data and MRI images. 
The model classifies records into the following categories: Non-Demented, Very Mild Dementia, Mild Dementia, and Moderate Dementia.

## Datasets
OASIS Dataset: Provided by the Washington University Alzheimer’s Disease Research Center.

- Numerical Data: Includes features like ID, Gender, Dominant Hand, Age, Education Level, Socioeconomic Status, MMSE, eTIV, nWBV, and CDR.
- Image Data: MRI Images

## Model Architecture

- Numerical Data: Random Forest with XGboost.
- MRI Images: Convolutional Neural Network (CNN).
- Integration: Late fusion of both models for final classification.

## Model Comparision for Numerical Data Algorithms:

## Algorithm: 

| Metric/Model        | Logistic Regression | SVM               | Random Forest      | KNN               |
|---------------------|---------------------|-------------------|--------------------|-------------------|
| **Accuracy**         | 0.945               | 0.896             | 0.990              | 0.791             |
| **Precision**        | 0.95           | 0.88              | 0.99               | 0.82              |
| **Recall**   | 0.95           | 0.90              | 0.99               | 0.79              |
| **F1-Score** | 0.94           | 0.89              | 0.99               | 0.80              |

### Performance-wise order of the models
1. Random Forest
2. Logistic Regression
3. SVM
4. KNN

## Booster: 

| Metric                | RF + AdaBoost | RF + Gradient Boosting | RF + XGBoost |
|-----------------------|-----------------------------------------|-------------------------------|---------------------------------|
| **Accuracy**           | 0.9502                                  | 0.9801                        | 0.9950                          |
| **Precision**| 0.67                                    | 0.97                          | 0.98                            |
| **Recall**   | 0.75                                    | 0.99                          | 0.99                            |
| **F1-Score** | 0.71                                    | 0.98                          | 0.98                            |

### Performance-wise order of the Boosters
1. XGBoost
2. Gradient Boosting
3. AdaBoost


