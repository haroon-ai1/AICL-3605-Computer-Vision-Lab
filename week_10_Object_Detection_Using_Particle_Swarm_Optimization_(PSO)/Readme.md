# Object Detection Using Particle Swarm Optimization (PSO) 🚀

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

**Course:** AICL 3605 - Computer Vision Lab  
**Author:** Muhammad Haroon  
**Registration Number:** 23108124  

## Overview
This repository contains a Python implementation of Particle Swarm Optimization (PSO) applied to object detection and 2D function optimization. The project demonstrates how swarm intelligence can be utilized to efficiently search for template matches within an image, as well as visualizing the convergence of particles on complex mathematical landscapes like the Ackley function.

## Features & Navigation Flow
The main logic and outputs are contained within the Jupyter Notebook (`Object_Detection_Using_Particle_Swarm_Optimization_(PSO).ipynb`), which is structured as follows:

1. **Code Example 1: Object Detection with PSO** Uses a custom fitness function integrating OpenCV's template matching (`cv2.matchTemplate`) to evaluate particle positions. Particles represent bounding box coordinates in the target scene, intelligently converging on the region that best matches a provided template image. The code includes a fallback to create dummy data if custom images are not provided.
2. **Code Example 2: 2D PSO Optimization & Visualization** Implements a generalized 2D PSO algorithm to find the global minimum of the Ackley function. Visualizes the optimization process using a 3D animated surface plot to illustrate how particles explore and exploit the search space over iterations.

## Technologies Used
* **Python 3.x**
* **OpenCV** (`cv2`)
* **NumPy**
* **Matplotlib** (for 3D surface plotting and animation)
* **IPython.display** (for rendering JS HTML animations)

## How to Run
> **Note:** This notebook is designed to be run in **Google Colab** as it utilizes Colab-specific patches like `cv2_imshow` and JavaScript HTML rendering for its animations.

1. Open the `.ipynb` file in Google Colab.
2. (Optional) Upload your own `scene.jpg` and `template.jpg` to the Colab environment for the object detection section to test on custom images.
3. Run the cells sequentially to observe the PSO template matching results and the 3D Ackley function optimization animation.

---

## Visual Results
Below are some highlights of the PSO algorithms applied during the project:

### 1. PSO Object Detection Match
*Bounding box predicted by the global best particle indicating the detected template in the scene.*
![Object Detection Match](Screenshots/Object_Detection_Match.png)

### 2. PSO 3D Convergence Animation
*Matplotlib animation showing particles converging on the global minimum of the 3D Ackley function landscape.*
![Ackley Function Convergence](Screenshots/Ackley_Function_Convergence.png)
