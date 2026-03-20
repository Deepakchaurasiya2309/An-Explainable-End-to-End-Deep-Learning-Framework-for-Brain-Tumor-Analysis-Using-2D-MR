# An-Explainable-End-to-End-Deep-Learning-Framework-for-Brain-Tumor-Analysis-Using-2D-MR
 It includes Data Preparation &amp;  preprocessing, segmentation using Attention U-Net, ROI extraction, and classification with Hybrid Classification Model. Handcrafted and deep features are fused and used by a Random Forest model for survival prediction. Guided Grad-CAM provides visual explanations, making the system accurate and interpretable.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Dataset Preparation</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;600&display=swap" rel="stylesheet">

<style>
body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #e3f2fd, #f8fbff);
    margin: 0;
    padding: 20px;
}

h1 {
    text-align: center;
    color: #2c3e50;
    margin-bottom: 30px;
}

.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
    max-width: 1100px;
    margin: auto;
}

.card {
    background: white;
    border-radius: 12px;
    padding: 18px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.08);
    transition: 0.3s ease;
    position: relative;
    overflow: hidden;
}

.card:hover {
    transform: translateY(-8px) scale(1.02);
    box-shadow: 0 12px 25px rgba(0,0,0,0.15);
}

.icon {
    font-size: 28px;
    margin-bottom: 10px;
}

.card h3 {
    margin: 5px 0;
    color: #34495e;
}

.card p {
    font-size: 14px;
    color: #555;
    line-height: 1.5;
}

/* subtle animation */
.card::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 4px;
    top: 0;
    left: 0;
    background: linear-gradient(90deg, #3498db, #6dd5fa);
}
</style>
</head>

<body>

<h1>📊 Dataset Preparation & Preprocessing</h1>

<div class="grid">

<div class="card">
<div class="icon">🧠</div>
<h3>Dataset Overview</h3>
<p>BRATS dataset includes multi-modal MRI (T1, T1ce, FLAIR) with tumor masks (~45GB 3D data).</p>
</div>

<div class="card">
<div class="icon">🔄</div>
<h3>3D to 2D Conversion</h3>
<p>3D volumes are sliced into 2D images for efficient GPU training and increased samples.</p>
</div>

<div class="card">
<div class="icon">🎯</div>
<h3>Multi-Modal Fusion</h3>
<p>Three MRI modalities combined into 3-channel images for better tumor representation.</p>
</div>

<div class="card">
<div class="icon">⚖️</div>
<h3>Slice Selection</h3>
<p>All tumor slices retained; only 20% non-tumor slices selected to balance data.</p>
</div>

<div class="card">
<div class="icon">📐</div>
<h3>Resizing</h3>
<p>All images resized to 160×160 resolution for consistency.</p>
</div>

<div class="card">
<div class="icon">📊</div>
<h3>Normalization</h3>
<p>Min-max normalization ensures stable and consistent pixel intensity values.</p>
</div>

<div class="card">
<div class="icon">🧩</div>
<h3>Mask Processing</h3>
<p>Masks resized using nearest-neighbor interpolation to preserve labels.</p>
</div>

<div class="card">
<div class="icon">💾</div>
<h3>Data Storage</h3>
<p>Saved as NumPy arrays for fast loading during training.</p>
</div>

<div class="card">
<div class="icon">🔁</div>
<h3>Data Augmentation</h3>
<p>Includes flipping and rotation to improve model generalization.</p>
</div>

<div class="card">
<div class="icon">📂</div>
<h3>Dataset Split</h3>
<p>80% training and 20% validation split used.</p>
</div>

<div class="card">
<div class="icon">🚀</div>
<h3>Final Outcome</h3>
<p>Dataset reduced from 45GB to 7GB, improving efficiency and performance.</p>
</div>

</div>

</body>
</html>

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
