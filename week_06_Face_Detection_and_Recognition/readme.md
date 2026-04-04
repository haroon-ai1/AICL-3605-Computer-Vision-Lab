# AICL-3605-Computer-Vision-Lab

## Week 06 - Face Detection using Haar Cascades

**Name:** Muhammad Haroon  
**Registration Number:** 23108124  

### 📝 Overview
This directory contains the implementation for Week 6 of the Computer Vision Lab. The focus of this week is on exploring and implementing **Face Detection** utilizing OpenCV's Haar Cascade Classifiers. The provided Jupyter notebook is designed to process both static images and video files to identify and draw bounding boxes around human faces.

### ⚙️ Implementation Details
The notebook covers the following core concepts:
* **Image Face Detection:** Uploading static images (JPG/PNG), converting them to grayscale, and identifying faces using the `haarcascade_frontalface_default.xml` model.
* **Video Face Detection:** Processing video files (e.g., MP4, AVI) frame-by-frame, applying the Haar Cascade classifier to detect faces, and visualizing the frames with bounding boxes. 
* **Dataset Handling:** Implementing a custom dataset loader to parse a structured face recognition dataset directory, extracting grayscale images, and organizing label dictionaries for training phases.

### 🛠️ Technologies & Libraries Used
* **Environment:** Google Colab
* **Programming Language:** Python 3
* **Libraries:** * `OpenCV (cv2)` for image processing and Haar Cascade execution.
    * `Matplotlib (pyplot)` for plotting and visualizing the output results.
    * `NumPy` for array handling.
    * `os` for directory parsing and dataset path management.
    * `google.colab.files` for handling media uploads directly within the Colab environment.

### 🚀 How to Run
1. Open the notebook (`Untitled33.ipynb`) in **Google Colab**.
2. Run the initial cells to import the required libraries and instantiate the Haar cascade classifier.
3. When prompted by the Colab upload widget, upload your desired image or video file.
4. The notebook will automatically process the media, apply the bounding boxes (green/blue rectangles), and display the output directly in the cell.
