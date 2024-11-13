# Mammogram Pectoral Muscle Removal and Classification

This repository contains the implementation of an advanced mammogram classification model using histo-sigmoid-based ROI clustering and a Support Value-based Deep Neural Network (SDNN). The project focuses on detecting breast cancer in mammograms by accurately removing the pectoral muscle and classifying mammogram images into normal, malignant, and benign categories. Experimental results show high accuracy, particularly on the MIAS and DDSM datasets.

## Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
- [Features Extracted](#features-extracted)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Datasets](#datasets)
- [Contributions](#contributions)
- [License](#license)

## Introduction

Breast cancer is one of the most common cancers among women, and early detection significantly reduces mortality rates. This project addresses the challenges in mammogram analysis by proposing a method to remove pectoral muscles from mammograms and classify images effectively using a custom neural network approach.

## Methodology

1. **Preprocessing**: We use Wiener filtering to reduce noise in the mammogram images.
2. **Histo-sigmoid-based ROI Clustering**: This algorithm is applied to separate the pectoral muscle from other breast tissue, making subsequent tumor detection more accurate.
3. **Feature Extraction**:
   - **Hough Transform**: For boundary detection.
   - **Discrete Cosine Transform (DCT)**: For frequency domain features.
4. **Classification**:
   - **Support Value-Based Adaptive Deep Neural Network (SDNN)**: This classifier uses convolutional, pooling, normalization, and fully connected layers, culminating in the classification of mammograms into normal, malignant, and benign categories.

## Features Extracted

The model relies on key extracted features:
- **Intensity Features**: Mean, variance, entropy, and standard deviation of the pixel intensities.
- **Shape Features**: Identified through the Hough Transform.
- **Texture Features**: Captured via DCT.

## Results

The proposed method demonstrates significant improvements in accuracy compared to existing techniques:
- **MIAS Dataset**: Achieved 99% accuracy.
- **DDSM Dataset**: Achieved 98% accuracy.

Comparisons with other classifiers (e.g., MSVM, MA-CNN) indicate that our method provides superior accuracy, sensitivity, and specificity.
## Usage

1. Preprocess images by applying Wiener filtering.
2. Run histo-sigmoid-based ROI clustering on preprocessed images.
3. Extract features and pass them through the SDNN model for classification.

## Datasets

We used two public datasets in this project:
- **MIAS Dataset**: Contains 322 digitized mammograms.
- **DDSM Dataset**: Consists of approximately 2,500 mammogram images for training and validation.
