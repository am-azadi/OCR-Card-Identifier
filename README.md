# OCR-Card-Identifier

This project focuses on enhancing card recognition and identification using deep learning and image processing techniques. The main objective is to accurately identify the type of card and extract relevant numeric data from both credit cards and national ID cards.

## Table of Contents
- [Overview](#overview)
- [Goals](#goals)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Methodologies](#methodologies)

## Overview
The OCR-Card-Identifier project leverages computer vision and deep learning methods to process images of cards. It identifies the type of card and extracts important numeric data, which can be in English or Farsi. The system aims to be robust, accurate, and efficient in various real-world scenarios.

## Goals
1. **Card Image Segmentation**: Identify and segment card areas from the image.
2. **Card Type Identification**: Determine if the card is a credit card or a national ID card.
3. **Numeric Data Localization**: Detect and extract numeric data fields on the card.
4. **Prediction of Numeric Data**: Predict numbers in both English and Farsi.

## Features
- **Card Type Detection**: Uses template matching for identifying card types.
- **National ID Card Processing**: Processes the entire image to recognize the dimensions of national ID cards and extract numeric data.
- **Credit Card Processing**: Detects edges and contours to locate the card number and other relevant information.
- **Deep Learning OCR**: Employs a custom OCR model with CTC (Connectionist Temporal Classification) loss for numeric prediction.

## Technologies Used
- Python
- OpenCV
- TensorFlow/Keras
- NumPy

## Methodologies
### Card Image Segmentation
1. **Edge Detection**: Uses OpenCV functions to detect edges and contours in the image.
2. **Contour Analysis**: Analyzes contours to locate and isolate the card region from the background.

### Card Type Identification
1. **Template Matching**: Compares card images against predefined templates for different card types (credit card, national ID card).
2. **Feature Extraction**: Extracts distinctive features from the card image to improve template matching accuracy.

### Numeric Data Localization
1. **Thresholding**: Applies binary thresholding to enhance numeric regions in the card image.
2. **Contour Detection**: Identifies contours around numeric data fields using OpenCV.
3. **Region of Interest (ROI) Extraction**: Extracts regions containing numeric data based on detected contours.

### Prediction of Numeric Data
1. **Deep Learning OCR Model**:
    - **Model Architecture**: A custom Convolutional Neural Network (CNN) designed for OCR tasks.
    - **CTC Loss Function**: Utilizes the Connectionist Temporal Classification (CTC) loss function to handle sequence prediction problems.
2. **Training Data**: Trained on a diverse dataset of numeric characters in both English and Farsi.
3. **Post-processing**: Applies post-processing techniques to refine predictions and improve accuracy.
