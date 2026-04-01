# vein-extraction-nir-cv
This project implements a classical computer vision pipeline to extract vein structures from NIR images. It uses Gaussian blur, CLAHE, top-hat transformation, and Frangi filtering for enhancement, followed by hybrid thresholding and morphological operations to generate a clean binary vein mask.
# Vein Extraction from NIR Images (Classical CV)

## 📌 Objective
To extract vein (vascular) structures from Near-Infrared (NIR) images using classical computer vision techniques and generate a clean binary mask.

## ⚙️ Pipeline Overview

The pipeline follows these steps:

1. **Input Image**
   - Load and resize grayscale NIR image.

2. **Noise Reduction**
   - Apply Gaussian Blur to remove high-frequency noise.

3. **Contrast Enhancement**
   - Use CLAHE to improve local contrast.

4. **Vein Enhancement**
   - Apply Top-hat transformation to highlight vein structures.
   - Use Frangi filter to enhance tubular (vessel-like) patterns.

5. **Segmentation**
   - Otsu Threshold → captures strong veins  
   - Adaptive Threshold → captures weak veins  
   - Combine both results

6. **Post-processing**
   - Apply morphological closing to remove small gaps and refine the mask.

---

## 🧪 Output
- Binary mask of veins (white on black background)
- Intermediate step-by-step outputs for analysis

---

## 🛠️ Tech Stack
- Python  
- OpenCV  
- NumPy  
- Scikit-image  
- Matplotlib  

---

## 📊 Results
The pipeline successfully extracts vein structures using only classical methods, without deep learning. It is lightweight, interpretable, and suitable for real-time applications.

---

## 🚀 How to Run
```bash
python your_script.py
