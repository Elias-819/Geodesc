# Geodesc

# 🧬 UAV Image Matching with Deep Learning

A lightweight implementation and demo for feature matching using **deep learning descriptors (GeoDesc)** applied to UAV imagery.

## 📖 Overview

This project explores a deep learning-based feature matching approach tailored for UAV (Unmanned Aerial Vehicle) remote sensing imagery. It investigates the integration of traditional descriptors like SIFT with learned descriptors like GeoDesc to improve robustness and accuracy in complex aerial scenes.

This repository accompanies the bachelor thesis:

> **"UAV Image Matching Method with Deep Learning Features"**  
> Author: Dongze Li  
> Institution: China University of Geosciences (Wuhan)  
> [📄 Download Thesis (PDF)](./videos/uav_matching_paper.pdf)

---

## 🔍 Motivation

Traditional handcrafted descriptors (e.g., SIFT, SURF) often fail in challenging conditions such as illumination changes, scale variance, and occlusion. Deep learning provides automatic feature extraction capabilities that can significantly boost matching performance in UAV applications like:

- Aerial mapping  
- Environmental monitoring  
- 3D reconstruction  
- Precision agriculture

---

## 🧠 Methodology

This work focuses on the **GeoDesc** method, which leverages a CNN-based architecture trained on the GL3D dataset. The main steps include:

- Feature extraction using a learned L2-Net-based architecture  
- Training with geometry-aware constraints and adaptive batch sampling  
- Evaluation via feature count and matching accuracy  
- Comparison with traditional descriptors (SIFT)

### 🔧 Key Techniques

- **Descriptors**: GeoDesc vs. SIFT  
- **Training data**: GL3D dataset (large-scale 3D UAV imagery)  
- **Feature learning**: L2-Net backbone, geometry-guided loss  
- **Evaluation metrics**:
  - Number of matched keypoints
  - Matching accuracy (%)

---

## 🧪 Experiments

| Image Pair | Descriptor | Keypoints | Matching Accuracy |
|------------|------------|-----------|-------------------|
| 4.3        | GeoDesc    | 946       | 72.6%             |
| 4.3        | SIFT       | 696       | 65.8%             |
| 4.4        | GeoDesc    | 1120      | 79.8%             |
| 4.4        | SIFT       | 923       | 74.3%             |

📈 Results show that **GeoDesc consistently outperforms SIFT** in both feature richness and matching accuracy.

---

## 🗂 Project Structure


---

## 📄 Related Work

- **GeoDesc**: Luo et al., *ECCV 2018*  
- **SIFT**: Lowe, *IJCV 2004*  
- **GL3D Dataset**: Large-scale UAV imagery for learning 3D geometry  
- **SFM**: Structure from Motion for 3D reconstruction

---


### Requirements

```bash
python>=3.6
numpy
opencv-python
tensorflow==1.14
matplotlib
