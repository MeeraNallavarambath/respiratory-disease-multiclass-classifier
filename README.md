# Respiratory Disease Multiclass Classifier

A deep learning system for classifying chest X-ray images into three categories: **Normal**, **Pneumonia**, and **COVID-19**.

## Project Overview

This project was developed as part of ACM40960 at University College Dublin. The goal is to build and evaluate deep learning models that can assist in the automated diagnosis of respiratory diseases from chest X-ray images.

## Dataset

-   **Source:** COVIDx-CXR dataset (Figshare)
-   **Size:** 3,225 radiologist-verified chest X-ray images
-   **Classes:** COVID-19, Normal, Pneumonia (balanced distribution)
-   **Split:** 80% training, 20% validation, separate test set (341 images)

## Models

| Model                        | Test Accuracy | COVID F1 | Normal F1 | Pneumonia F1 |
|---------------------|-------------|-------------|-------------|-------------|
| Baseline CNN                 | 73%           | 0.80     | 0.77      | 0.63         |
| ResNet50 (Transfer Learning) | 78%           | 0.77     | 0.91      | 0.65         |

## Project Structure
```
respiratory-disease-multiclass-classifier/
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_baseline_model.ipynb
│   ├── 04_resnet_model.ipynb
│   └── 05_evaluation.ipynb
├── results/
│   └── confusion_matrices.png
├── data/
│   └── (not included - see reproduction instructions)
└── models/
    └── (not included - run notebooks to reproduce)
```
## Key Findings

-   ResNet50 outperformed the baseline CNN by \~5% on test accuracy
-   Both models struggled most with Pneumonia classification
-   COVID and Pneumonia were most commonly confused — clinically expected as both conditions cause similar lung inflammation on X-rays
-   ResNet50 significantly improved Normal classification (F1: 0.77 → 0.91)

## Reproducing Results

1.  Clone the repository
2.  Install dependencies: `pip install torch torchvision pillow numpy pandas matplotlib seaborn scikit-learn`
3.  Download the COVIDx-CXR dataset from Figshare and place in `data/Dataset/`
4.  Run notebooks in order (01 → 05)

## Team

-   Meera Nallavarambath (25212715)
-   Anushree Neerulli Sudhakara (24216584)

**Supervisor:** Dr. Sarp Akçay \| ACM40960 \| University College Dublin
