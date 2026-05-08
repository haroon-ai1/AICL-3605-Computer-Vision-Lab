# Lab 07: Implementation of Gabor Feature Extraction 🚀

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

**Course:** AICL 3605 - Computer Vision Lab  
**Author:** Muhammad Haroon  
**Registration Number:** 23108124  

## Overview
This repository contains a Python and OpenCV implementation of Gabor Feature Extraction. The project explores the use of Gabor filters for spatial frequency analysis and texture extraction. It demonstrates how to apply individual Gabor kernels to highlight specific directional frequencies, and extends this by utilizing a comprehensive bank of Gabor filters to extract statistical features (mean and variance) to train a Support Vector Machine (SVM) for automated texture recognition.

## Features & Navigation Flow
The main logic and outputs are contained within the Jupyter Notebook (`LAB_07Implementation_of_Gabor_Feature_Extraction.ipynb`), which is structured sequentially:

1. **Code Example 1: Basic Gabor Filtering** Uploads a target image (e.g., texture, face, fingerprint) and applies a specialized Gabor kernel (configured with specific size, sigma, theta, lambda, and gamma) to extract directional features and structural details.
2. **Case Study 1: Texture Classification using Gabor Filter Banks & SVM** Uploads a dataset of various texture images, generates a filter bank to extract robust feature vectors, and trains a Support Vector Machine (SVM) to classify and predict the texture labels of test data, printing the model's overall accuracy.

## Technologies Used
* **Python 3.x**
* **OpenCV** (`cv2`)
* **NumPy**
* **Matplotlib** (for visualizations)
* **Scikit-Learn** (for SVM classification and accuracy metrics)

## How to Run
> **Note:** This notebook is specifically designed to be run in **Google Colab** as it utilizes `google.colab import files` for dynamic image uploading.

1. Open the `.ipynb` file in Google Colab.
2. Run the cells sequentially.
3. When prompted by the execution output, upload the respective sample images (e.g., a grayscale fingerprint, or a batch of texture dataset images) from your local machine to see the Gabor filter and SVM classification algorithms in action.

---

## Visual Results
Below are some highlights of the feature extraction and classification algorithms applied during the lab:

### 1. Gabor Filtered Image
*Extracting specific directional features and textures using a single Gabor kernel.*
![Gabor Filtered Image](Screenshots/Gabor_Filtered_Image.png)

### 2. Texture Classification Predictions
*Predicting and visualizing texture classes using an SVM trained on Gabor filter bank features.*
![Texture Classification](Screenshots/Texture_Classification.png)
