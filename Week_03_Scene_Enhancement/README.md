# Lab 03: Scene Enhancement using Point Processing Techniques

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

**Course:** AICL 3602 - Computer Vision Lab  
**Student Name:** Muhammad Haroon  
**Registration Number:** 23108124  
**Topic:** Contrast Enhancement (SPTAIS)

---

## 📌 TASK Overview
This repository contains the implementation of **Point Processing Techniques** to improve image quality and visual clarity. These methods are fundamental in Computer Vision for preprocessing images captured in challenging environments.

### 🛠 Key Techniques Implemented
1.  **Linear Contrast Stretching**: Normalizing intensity to the full 0-255 range.
2.  **Histogram Equalization**: Distributing pixel intensities to enhance global contrast.
3.  **Power-Law (Gamma) Correction**: Adjusting brightness non-linearly using $\gamma$ values.

---

## 🧪 Real-World Case Studies
I applied these techniques to solve five specific industry scenarios:

| Case Study | Scenario | Core Technique |
| :--- | :--- | :--- |
| **01** | **Marine Biology** | Histogram Equalization for underwater clarity. |
| **02** | **Satellite Imaging** | Gamma Correction for terrain details. |
| **03** | **Surveillance** | Equalization for low-light security frames. |
| **04** | **OCR Preparation** | CLAHE (Adaptive Equalization) for text scans. |
| **05** | **Driver Assistance** | Contrast Stretching + Gamma for foggy roads. |

---

## 🚀 How to Run
1. Open the notebook in **Google Colab**.
2. Run the initialization cells to load libraries.
3. Upload your sample image when prompted by `files.upload()`.
4. View the results and histogram plots generated automatically.

## 📊 Sample Results Visualization


The project includes histogram visualizations to prove the mathematical shift in pixel distribution from a narrow range to a balanced spectrum.

---
*Developed as part of the Robotics & Artificial Intelligence department curriculum at SZABIST.*
