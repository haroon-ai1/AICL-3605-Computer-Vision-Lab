# LAB #08 — Implementation of Content-Based Image Retrieval (CBIR)

## 📖 Overview
This lab explores **Content-Based Image Retrieval (CBIR)**, a technique that retrieves visually similar images from a database by analyzing their **visual content** (color, texture, shape) rather than relying on textual metadata or tags.

CBIR systems extract numerical **feature vectors** from images and use **similarity/distance metrics** (e.g., correlation, cosine similarity, Chi-Square distance) to rank database images against a query image. This lab demonstrates CBIR across multiple real-world domains including art, wildlife research, fabric inspection, fashion e-commerce, and medical imaging.

---

## 🎯 Objectives
- Understand the working principles of Content-Based Image Retrieval (CBIR).
- Extract visual features using **Color Histograms (RGB / HSV)** and **Local Binary Patterns (LBP)**.
- Compare images using similarity metrics: **Correlation**, **Cosine Similarity**, and **Chi-Square Distance**.
- Apply CBIR to practical domains: art retrieval, wildlife analysis, textile defect detection, fashion search, and medical imaging.
- Visualize and rank the top-K most similar images for a given query.

---

## 🧠 Concepts Covered
| Concept | Description |
|---------|-------------|
| **Color Histogram** | Statistical distribution of pixel color intensities used as a global descriptor. |
| **HSV Color Space** | Perceptually meaningful color representation (Hue, Saturation, Value). |
| **Local Binary Pattern (LBP)** | Texture descriptor that encodes local pixel neighborhood patterns. |
| **Histogram Correlation** | Measures linear similarity between two histograms. |
| **Cosine Similarity** | Measures the angle between two feature vectors. |
| **Chi-Square Distance** | Measures dissimilarity between two distributions (lower = more similar). |

---

## 🛠️ Tools & Libraries
- **Python 3**
- **OpenCV (cv2)** — image loading, color space conversion, histogram computation
- **NumPy** — numerical operations
- **Matplotlib** — visualization of query and retrieved images
- **scikit-image** — Local Binary Pattern (LBP) feature extraction
- **scikit-learn** — cosine similarity computation
- **Kaggle API** — dataset access (KTH-TIPS-2, DeepFashion, Brain Tumor MRI)

---

## 📂 Notebook Structure

### 🔹 Code Example 1 — Color Histogram CBIR (Digital Art Museum)
**Scenario:** A digital art museum CBIR system retrieves similar artworks using **RGB color histogram correlation**.
- **Dataset:** TensorFlow `flower_photos` (auto-downloaded)
- **Feature:** 3D RGB histogram (8×8×8 bins)
- **Similarity Metric:** `cv2.HISTCMP_CORREL`
- **Output:** Top 3 visually similar images to the query.

### 🔹 Code Example 2 — HSV Color CBIR (Wildlife Research)
**Scenario:** A wildlife research center retrieves similar tiger images using **HSV histograms + cosine similarity**.
- **Dataset:** Custom wildlife image URLs (tiger, lioness, forest cat)
- **Feature:** 3D HSV histogram (8×8×8 bins)
- **Similarity Metric:** Cosine Similarity
- **Output:** Ranked visually similar wildlife images.

### 🔹 Code Example 3 — LBP Texture CBIR (Fabric Defect Detection)
**Scenario:** A textile manufacturer automates quality inspection using **Local Binary Patterns** to detect fabric defects.
- **Dataset:** KTH-TIPS-2 (via Kaggle API)
- **Feature:** Uniform LBP (P=24, R=3)
- **Similarity Metric:** Chi-Square Distance
- **Output:** Top 3 textures most similar to the query.

### 🔸 Case Study 1 — Fashion E-Commerce Image Search
**Scenario:** An online fashion retailer enables **visual product search** — customers upload a clothing photo, and the system finds similar catalog items.
- **Dataset:** DeepFashion (via Kaggle API)
- **Feature:** HSV color histogram
- **Similarity Metric:** Cosine Similarity
- **Output:** Top 3 similar fashion items.

### 🔸 Case Study 2 — Medical Imaging Retrieval
**Scenario:** Radiologists retrieve visually similar past MRI scans to support diagnosis and treatment planning.
- **Dataset:** Brain Tumor MRI Dataset (via Kaggle API)
- **Feature:** Grayscale histogram (256 bins)
- **Similarity Metric:** Cosine Similarity
- **Output:** Top 3 similar MRI scans.

---

## ⚙️ Setup & Requirements

### Install Dependencies
```bash
pip install opencv-python numpy matplotlib scikit-image scikit-learn
```

### Kaggle API Configuration
Code Examples 3 and the Case Studies require Kaggle dataset access:
1. Go to [Kaggle Account Settings](https://www.kaggle.com/account)
2. Click **Create New API Token** to download `kaggle.json`
3. Upload `kaggle.json` when prompted in the notebook
```python
from google.colab import files
files.upload()  # upload kaggle.json
```

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/haroon-ai1/AICL-3605-Computer-Vision-Lab.git
   ```
2. Open the notebook in **Google Colab** (recommended) or **Jupyter**:
   ```
   WEEK_8_Content_Based_Image_Retrieval__CBIR_.ipynb
   ```
3. Run cells sequentially from top to bottom.
4. Upload `kaggle.json` when prompted (for Kaggle-based examples).
5. View the query image alongside the top-K retrieved matches.

---

## 📊 Expected Output
For each example, the notebook displays:
- The **Query Image** on the left.
- The **Top-3 Retrieved Matches** with their similarity/distance scores.
- A descriptive title indicating which CBIR method was used.

---

## 🧪 Key Takeaways
- **Color histograms** work well for retrieval tasks dominated by color (art, fashion).
- **HSV space** is more robust to illumination variation than RGB.
- **LBP features** are highly effective for texture-based retrieval (fabrics, materials).
- **Choice of similarity metric** significantly impacts retrieval quality.
- CBIR provides the foundation for modern image search engines, reverse-image lookup, medical image retrieval, and visual product search.

---

## 👨‍🎓 Course Information
- **Course:** AICL-3605 — Computer Vision Lab
- **Lab #:** 08
- **Topic:** Content-Based Image Retrieval (CBIR)

---

## 📎 References
- Smeulders, A.W.M. et al. (2000). *Content-based image retrieval at the end of the early years.* IEEE TPAMI.
- Ojala, T., Pietikäinen, M., & Mäenpää, T. (2002). *Multiresolution gray-scale and rotation invariant texture classification with local binary patterns.* IEEE TPAMI.
- OpenCV Documentation — [Histograms](https://docs.opencv.org/4.x/de/db2/tutorial_py_table_of_contents_histograms.html)
- scikit-image Documentation — [Local Binary Pattern](https://scikit-image.org/docs/stable/auto_examples/features_detection/plot_local_binary_pattern.html)
