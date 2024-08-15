# Alzheimer's Disease Diagnosis Using Multimodal Deep Learning

This project develops a multimodal model to assess Alzheimer's disease using numerical data and MRI images. The model classifies records into the following categories: Non-Demented, Very Mild Dementia, Mild Dementia, and Moderate Dementia.

## Datasets
OASIS Dataset: Provided by the Washington University Alzheimer’s Disease Research Center.

- Numerical Data: Includes features like ID, Gender, Dominant Hand, Age, Education Level, Socioeconomic Status, MMSE, eTIV, nWBV, and CDR.
- Image Data: MRI Images

## Model Architecture

- Numerical Data: Decision Tree with Gradient Boosting.
- MRI Images: Convolutional Neural Network (CNN).
- Integration: Late fusion of both models for final classification.
