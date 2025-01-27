# Alzheimer's Disease Diagnosis Using Multi-modal Learning

This project develops a multimodal model to assess Alzheimer's disease using numerical data and MRI images. 
The model classifies records into the following categories: Non-Demented, Mild Dementia, Moderate Dementia, and Severe Dementia.

## Datasets
OASIS Dataset: Provided by the Washington University Alzheimer’s Disease Research Center.

- Numerical Data: Includes features like ID, Gender, Dominant Hand, Age, Education Level, Socioeconomic Status, MMSE, eTIV, nWBV, and CDR.
- Image Data: MRI Images

![image](https://github.com/user-attachments/assets/79cf2858-76f9-4772-a195-aba66d1f7e11)

## Model Architecture

- Numerical Data: Random Forest with XGboost.
- MRI Images: Convolutional Neural Network (CNN).
- Integration: Late fusion of both models for final classification.

## Model Comparision for Numerical Data Algorithms:

## Algorithm: 

| Algorithm                   | Accuracy | Precision | Recall | F1-Score | Loss | Cohen Kappa Score | Matthews Corr. Coeff. | Hamming Loss | Weighted Jaccard |
|-----------------------------|----------|-----------------|--------------|----------------|----------|-------------------|-----------------------|--------------|------------------|
| **K-Nearest Neighbors**     | 0.791    | 0.82            | 0.79         | 0.80           | 2.140    | 0.672             | 0.674                 | 0.209        | 0.705            |
| **Support Vector Machine**  | 0.896    | 0.88            | 0.90         | 0.89           | 0.278    | 0.831             | 0.832                 | 0.104        | 0.837            |
| **Logistic Regression**     | 0.945    | 0.95            | 0.95         | 0.94           | 0.178    | 0.912             | 0.913                 | 0.055        | 0.904            |
| **Random Forest**           | 0.995    | 9.98            | 9.98         | 9.96           | 0.135    | 0.992             | 0.992                 | 0.005        | 0.991            |


### Performance-wise order of the models
1. Random Forest
2. Logistic Regression
3. SVM
4. KNN

## Booster: 

| Algorithm                                | Accuracy | Precision | Recall | F1-Score | Loss | Cohen Kappa Score | Matthews Corr. Coeff. | Hamming Loss | Weighted Jaccard |
|------------------------------------------|----------|-----------------|--------------|----------------|----------|-------------------|-----------------------|--------------|------------------|
| **AdaBoost + Random Forest**     | 0.9502   | 0.9156          | 0.9502       | 0.9298         | 0.1031   | 0.9192           | 0.9230               | 0.0498       | 0.9156           |
| **Gradient Boosting + Random Forest** | 0.9851   | 0.9853          | 0.9851       | 0.9851         | 0.0544   | 0.9759           | 0.9760               | 0.0149       | 0.9706           |
| **Random Forest + XGBoost** | 0.9950   | 0.9955          | 0.9950       | 0.9951         | 0.0659   | 0.9920           | 0.9920               | 0.0050       | 0.9905           |

### Performance-wise order of the Boosters
1. XGBoost
2. Gradient Boosting
3. AdaBoost

# CNN Performance Comparison


| Model         | Final Training Loss | Final Validation Loss | Final Training Accuracy | Final Validation Accuracy |
|---------------|---------------------|-----------------------|-------------------------|---------------------------|
| **Xception**     | 0.0056              | 0.0071               | 0.9998                     | 0.9951                       |
| **MobileNetV2** | 0.0247             | 0.0233               | 0.9913                     | 0.9951                        |
| **ResNet50**  | 0.0534              | 0.0552               | 0.9962                  | 0.9851                    |
| **InceptionV3** | 0.0542             | 0.0947               | 0.9912                  | 0.9851                    |
| **CNN1**      | 0.4633              | 0.4099               | 0.8063                  | 0.9303                    |
| **CNN2**      | 1.1722              | 1.2789               | 0.4931                  | 0.4876                    |

