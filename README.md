# An-Explainable-End-to-End-Deep-Learning-Framework-for-Brain-Tumor-Analysis-Using-2D-MR
 It includes Data Preparation &amp;  preprocessing, segmentation using Attention U-Net, ROI extraction, and classification with Hybrid Classification Model. Handcrafted and deep features are fused and used by a Random Forest model for survival prediction. Guided Grad-CAM provides visual explanations, making the system accurate and interpretable.

# 📊 Dataset Preparation & Preprocessing

## 🧠 Dataset Overview
BRATS dataset contains multi-modal MRI scans (T1, T1ce, FLAIR) with tumor masks (~45GB 3D data).

## 🔄 3D to 2D Conversion
Converted 3D MRI volumes into 2D slices for efficient training and increased dataset size.

## 🎯 Multi-Modal Fusion
Combined T1, T1ce, and FLAIR into 3-channel images.

## ⚖️ Slice Selection
- All tumor slices retained  
- Only 20% non-tumor slices selected  

## 📐 Resizing
Images resized to **160×160** resolution.

## 📊 Normalization
Applied **min-max normalization** for stable intensity values.

## 🧩 Mask Processing
Used nearest-neighbor interpolation for segmentation masks.

## 💾 Data Storage
Saved as **NumPy arrays** for efficient loading.

## 🔁 Data Augmentation
Applied:
- Horizontal & vertical flips  
- Small rotations  

## 📂 Dataset Split
- 80% Training  
- 20% Validation  

## 🚀 Final Outcome
Dataset reduced from **45GB → 7GB**, improving efficiency while preserving tumor features.
