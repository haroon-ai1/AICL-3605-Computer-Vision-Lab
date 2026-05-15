# LAB #09 — Implementation of Object Detection and Recognition

## 📖 Overview
This lab introduces **Object Detection and Recognition** — the task of finding **where** objects are in an image (localization) and **what** they are (classification) at the same time.

Unlike image classification (which only labels the whole image), object detection draws **bounding boxes** around every object of interest and assigns each one a **class label** and a **confidence score**. In this lab we work hands-on with three different detection paradigms — classical and modern — and apply them to five real-world inspired case studies.

---

## 🎯 Objectives
- Distinguish between **image classification**, **object detection**, and **recognition**.
- Run inference using both **classical** detectors (Haar Cascade, HOG + SVM) and **deep learning** detectors (YOLOv8).
- Read and interpret YOLO output — class IDs, confidence scores, and bounding-box coordinates.
- Build a small **multi-detector application** for a chosen problem domain.
- Compare detector performance qualitatively on the same input image.

---

## 🧠 Concepts Covered
| Concept | Description |
|---------|-------------|
| **Haar Cascade** | Classical detector based on Haar-like features + AdaBoost (Viola–Jones, 2001). |
| **HOG + SVM** | Histogram of Oriented Gradients with a linear SVM (Dalal & Triggs, 2005). |
| **YOLOv8** | Modern one-stage deep-learning detector — fast and multi-class. |
| **Bounding Box** | Rectangular region `(x1, y1, x2, y2)` localizing an object. |
| **Confidence Score** | Probability that a detection is correct (0.0 – 1.0). |
| **COCO Dataset** | 80-class benchmark dataset YOLOv8 is pre-trained on. |

---

## 🛠️ Tools & Libraries
- **Python 3.x**
- **OpenCV (cv2)** — image I/O, Haar Cascade, HOG+SVM, drawing
- **Ultralytics YOLOv8** — pre-trained deep-learning detector
- **NumPy** — numerical operations
- **Matplotlib** — visualization
- **Pillow & Requests** — image downloading utilities

---

## 📂 Notebook Structure

### 🔹 Part 1 — Environment Setup
- Install dependencies (`ultralytics`, `opencv-python-headless`, etc.).
- Define utility functions: `fetch_image()`, `display_bgr()`, `display_side_by_side()`.

### 🔹 Part 2 — Loading the YOLOv8 Model
- Load the YOLOv8 nano variant (`yolov8n.pt`).
- Inspect the 80 COCO class labels.
- Run a sanity-check inference and parse the structured output.

### 🔹 Part 3 — Classical Detectors (for Comparison)
- **Haar Cascade** for face detection.
- **HOG + SVM** for pedestrian detection.
- Side-by-side visual comparison of Haar vs HOG vs YOLOv8 on the same image.

### 🔸 Part 4 — Real-World Case Studies

| # | Case Study | Detection Targets |
|---|------------|-------------------|
| **A** | Urban Traffic Analytics | car, truck, bus, motorcycle, bicycle |
| **B** | Drone-Based Search & Rescue | person (with confidence threshold) |
| **C** | Sports Analytics | person, sports ball, racket, bat |
| **D** | Warehouse Inventory Audit | bottle, cup, book, laptop, etc. |
| **E** | Precision Agriculture Field Survey | apple, orange, banana |

Each case study follows the same pattern: **scenario → detection → structured report**.

### 🔹 Part 5 — Summary & Reflection
- Detector trade-off table (speed vs accuracy vs flexibility).
- 4 reflection questions for self-assessment.

---

## ⚙️ Setup & Requirements

### Install Dependencies
```bash
pip install ultralytics opencv-python-headless matplotlib pillow requests numpy
```

> **Note:** The first time `YOLO("yolov8n.pt")` is called, the model weights (~6 MB) will be downloaded automatically.

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/AICL-3605-Computer-Vision-Lab.git
   ```
2. Open the notebook in **Google Colab** (recommended) or **Jupyter**:
   ```
   Lab_09_Object_Detection.ipynb
   ```
3. Run cells sequentially from top to bottom (no manual uploads required — all images are fetched from public URLs).
4. View the annotated detections and structured reports for each case study.

---

## 📊 Expected Output
For each section, the notebook produces:
- An **annotated image** with bounding boxes, class labels, and confidence scores.
- A **structured text report** (e.g., traffic composition, attendance log, inventory audit).
- For Part 3 — a **side-by-side comparison plot** of all three detectors.

---

## 🧪 Detector Trade-offs

| Detector | Speed | Accuracy | Multi-class | Best For |
|---|---|---|---|---|
| **Haar Cascade** | Very fast | Low–Medium | ❌ | Lightweight face/eye detection on CPU |
| **HOG + SVM** | Fast | Medium | ❌ | Pedestrian detection without GPU |
| **YOLOv8-nano** | Fast (faster on GPU) | High | ✅ (80 classes) | General-purpose modern detection |

---

## 🧩 Key Takeaways
- Deep learning detectors (YOLOv8) outperform classical detectors (Haar, HOG) on multi-class tasks.
- Pre-trained models let you build real applications without collecting training data.
- The **confidence threshold** is a critical hyperparameter — it controls the precision/recall trade-off.
- Object detection has diverse industry applications: traffic monitoring, disaster response, sports analytics, inventory management, and precision agriculture.

---

## 👨‍🎓 Course Information
- **Course:** AICL-3602 — Computer Vision Lab
- **Lab #:** 09
- **Topic:** Object Detection and Recognition

---

## 📎 References
- Viola, P., & Jones, M. (2001). *Rapid Object Detection using a Boosted Cascade of Simple Features.* CVPR.
- Dalal, N., & Triggs, B. (2005). *Histograms of Oriented Gradients for Human Detection.* CVPR.
- Redmon, J. et al. (2016). *You Only Look Once: Unified, Real-Time Object Detection.* CVPR.
- Ultralytics YOLOv8 Documentation — [https://docs.ultralytics.com](https://docs.ultralytics.com)
- OpenCV Documentation — [https://docs.opencv.org](https://docs.opencv.org)
- COCO Dataset — [https://cocodataset.org](https://cocodataset.org)
