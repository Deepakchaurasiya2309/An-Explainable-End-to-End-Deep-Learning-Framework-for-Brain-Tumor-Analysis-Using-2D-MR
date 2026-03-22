# An-Explainable-End-to-End-Deep-Learning-Framework-for-Brain-Tumor-Analysis-Using-2D-MRI
 It includes Data Preparation &amp;  preprocessing, segmentation using Attention U-Net, ROI extraction, and classification with Hybrid Classification Model. Handcrafted and deep features are fused and used by a Random Forest model for survival prediction. Guided Grad-CAM provides visual explanations, making the system accurate and interpretable.

<p align="center">
  <div style="display: flex; justify-content: center; gap: 20px;">
    <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExMDU1MTFzNmo0aWU4NjdqbGRwamRlYWpwZ2ZsN3cxcnc1aDI2YmM1eCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/RqxdeXRrOiGic/giphy.gif" 
         alt="Brain MRI Visualization" 
         width="30%" />
    <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjJlcmJwNjAzbzg4YWdkenhicmFqanI1OHI0cmV1YnRhM2x1cW52MSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Vn9JVHDAzYw1O/giphy.gif" 
         alt="Brain MRI Visualization" 
         width="30%" />
         <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExOW85dmxtdzJxenRwcmQxOHJ2MjZkaXNwaHRibmlxbXM4b3piOGU1diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/26FmPPUf4XbpURNdu/giphy.gif" 
         alt="Brain MRI Visualization" 
         width="30%" />
   
  </div>
</p>
 <h2>🧠 Brain Tumor Analysis: Working Procedure</h2>

<div>

  <!-- Step 1 -->
  <div>
    <img src="<img width="1366" height="768" alt="Overrall_Project_pipline_Output" src="https://github.com/user-attachments/assets/ec447036-9970-4067-92d1-69241336af01" />
" width="32" alt="MRI ">
    <div>
      <b>1️⃣ Raw 2D MRI Slices </b><br>
      Resize, normalize, select slices, augment
    </div>
  </div>

  <!-- Step 2 -->
  <div>
    <img src="![Data_Preperation_and_Preprocessing](https://github.com/user-attachments/assets/aea9ba9c-7178-4da3-9d94-9094a04dcc75)
" width="32" alt="Dataset Icon">
    <div>
      <b>2️⃣ Dataset Preparation</b><br>
      Resize, normalize, augment, split training/validation
    </div>
  </div>

  <!-- Step 3 -->
  <div>
    <img src="<img width="960" height="636" alt="Segmentation_output" src="https://github.com/user-attachments/assets/aa9c9053-d4dd-41c6-99e5-18f3de7bac25" />
" width="32" alt="Segmentation ">
    <div>
      <b>3️⃣ Tumor Segmentation (Attention U-Net)</b><br>
      ROI extraction, binary tumor mask
    </div>
  </div>

  <!-- Step 4 -->
  <div>
    <img src="![Classification_Hybrid _Model](https://github.com/user-attachments/assets/28191032-6167-47fb-892f-f84e19a6ff3e)
" width="32" alt="Tumor Icon">
    <div>
      <b>4️⃣ Tumor Grading (Hybrid ResNet50)</b><br>
      Classify No Tumor / LGG / HGG
    </div>
  </div>

  <!-- Step 5 -->
  <div>
    <img src="![Survival Prediction And Explainable AI](https://github.com/user-attachments/assets/a6a0cfb8-4502-4019-95b3-4dffeccc4159)
" width="32" alt="Fusion">
    <div>
      <b>5️⃣ Feature Fusion & Survival Prediction</b><br>
      Deep + spatial features → Random Forest prediction
    </div>
  </div>

  <!-- Step 6 -->
  <div>
    <img src="<img width="1366" height="482" alt="Survival Prediction                                  Explainable AI" src="https://github.com/user-attachments/assets/f04a5775-0324-4c64-adc5-1e61d8acf9e8" />
" width="32" alt="Grad-CAM ">
    <div>
      <b>6️⃣ Explainable AI (Grad-CAM)</b><br>
      Highlight important tumor regions
    </div>
  </div>

</div>
 # 🧠 Brain Tumor Analysis: Working Procedure

A clear visual overview of the **end-to-end workflow** for 2D MRI brain tumor analysis.

---
## 🏗️ Workflow Structure

```text
        ┌───────────────┐
        │ Raw 2D MRI    │
        │ Slices Input  │
        └───────┬───────┘
                │
                ▼
        ┌───────────────┐
        │ 1️⃣ Dataset   │
        │ Preparation   │
        │ • Resize &    │
        │   Normalize   │
        │ • Slice       │
        │   Selection   │
        │ • Augmentation│
        └───────┬───────┘
                │
                ▼
        ┌───────────────┐
        │ 2️⃣ Segmentation│
        │ (Attention    │
        │  U-Net)       │
        │ • Tumor ROI   │
        │   Extraction  │
        └───────┬───────┘
                │
                ▼
        ┌───────────────┐
        │ 3️⃣ Tumor     │
        │ Grading       │
        │ (Hybrid      │
        │ ResNet50)     │
        │ • Classify   │
        │   No Tumor / │
        │   LGG / HGG  │
        └───────┬───────┘
                │
                ▼
        ┌───────────────┐
        │ 4️⃣ Feature   │
        │ Fusion        │
        │ • Deep +      │
        │   Spatial     │
        │   Features    │
        │ • Multimodal  │
        │   Vector      │
        └───────┬───────┘
                │
                ▼
        ┌───────────────┐
        │ 5️⃣ Survival   │
        │ Prediction     │
        │ (Random Forest)│
        │ • Risk / Survival│
        │   Prediction   │
        └───────┬───────┘
                │
                ▼
        ┌───────────────┐
        │ 6️⃣ Explainable│
        │ AI (Grad-CAM) │
        │ • Highlight   │
        │   Important   │
        │   Tumor Areas │
        └───────────────┘



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


# 🧠 Tumor Segmentation Using Attention U-Net Model

Accurate tumor segmentation is a critical step in automated brain tumor analysis, as it directly affects downstream tasks like classification, feature fusion, and survival prediction. The proposed system uses an **Attention U-Net** architecture to achieve precise tumor localization from 2D MRI slices.

## 🎯 Input
- MRI slice: `I ∈ R^(H×W×C)`  
- H, W → spatial dimensions  
- C = 3 (multi-modal channels: T1, T1ce, FLAIR)

## 🔍 Motivation
- Tumor regions are small, heterogeneous, and surrounded by complex anatomy.  
- Traditional U-Net limitations:
  - Includes irrelevant background  
  - Reduced sensitivity to small tumors  
  - Poor localization in low-contrast areas  

**Attention U-Net** solves these by using attention gates to focus on salient tumor regions and suppress irrelevant background.

## ⚙️ Architecture
- **Encoder:** Extracts hierarchical features using convolutional blocks  
- **Decoder:** Recovers spatial resolution using transposed convolutions  
- **Attention Gates:** Filter irrelevant activations in skip connections  
- M → predicted mask, G → ground truth

## ⚡ Training Details
- Optimizer: Adam  
- Mixed-precision training for efficiency  
- Dataset:
  - Training: 2400 slices  
  - Validation: 600 slices  
- Epochs: 5  

## ✅ Advantages of Attention U-Net
| Model Type | Limitation | Expected Performance |
|------------|------------|--------------------|
| Basic CNN | Poor spatial localization | Low |
| Standard U-Net | No feature selection | Moderate |
| Fully Deep Models | High computational cost | High but expensive |
| **Attention U-Net (Proposed)** | Selective focus on tumor regions | Balanced & efficient |

**Key benefits:**
- Reduces false positives by suppressing background  
- Enhances detection of small tumors  
- Improves generalization in limited-data scenarios  

## ✂️ Segmentation-Based ROI Extraction
- Extracted smallest bounding box around foreground pixels  
- Cropped to form ROI → removes background  
- ROI resized to a constant resolution for classification  
- If no tumor detected, full slice retained  

---

# 🎓 Tumor Grading/Classification Using Hybrid Deep Learning

Tumor grading is performed using a **hybrid deep learning architecture** designed to overcome limitations of conventional models in medical imaging, such as limited annotated data and overfitting risks.

## 🔹 Motivation
- Medical datasets are often small, making training deep CNNs from scratch prone to overfitting.  
- Traditional CNNs may fail to capture high-level semantic features.  
- Fully trainable deep models require large datasets and high computational resources.  

The hybrid model leverages **pre-trained networks** to overcome these challenges.

## ⚙️ Model Architecture
- **Backbone:** Pre-trained ResNet50  
  - Used as a **fixed feature extractor**  
  - Backbone parameters frozen to prevent overfitting  
  - Fully connected layer removed to produce deep features:
 
- **Classification Head:**  
- Lightweight fully connected layers  
- ReLU activation + Dropout regularization  
- Maps deep features into 3 diagnostic classes:
  1. No Tumor  
  2. Low-Grade Glioma (LGG)  
  3. High-Grade Glioma (HGG)
     
****  This hybrid approach leverages robust pre-trained features from ResNet50 while focusing on task-specific classification with a lightweight head. It ensures efficient learning on small medical datasets and produces reliable tumor grading predictions.


# 🔗 Multimodal Feature Fusion & Survival Prediction

## 🌟 Multimodal Feature Fusion
Deep CNN features capture semantic information well but may miss quantitative tumor details like size or shape. To address this, **handcrafted spatial features** are added to deep features.

- **Tumor Volume (V):**  
V = sum of all foreground pixels in the segmentation mask (M_ij)

- **Tumor Area Ratio (R):**  
R = V / (H × W)  
(H × W = spatial size of the image)

- **Feature Fusion:**  
F_fusion = [F_deep, V, R]  
This combines **semantic (deep features)** and **geometric/spatial information**, improving predictive accuracy.

---

## 🏥 Survival Prediction
Survival prediction uses the fused multimodal features from deep learning and tumor morphology.

- **Fused Feature Vector:**  
F_fusion = {F_deep, V_tumor, R_area}  
  - F_deep = high-level deep features from ResNet50 (size 2048)  
  - V_tumor = tumor volume from segmentation  
  - R_area = normalized tumor area ratio  

- **Prediction Model:** Random Forest Classifier  
s_hat = f_RF(F_fusion)  
  - f_RF = ensemble of decision trees  
  - Final prediction = average output of all trees  

**Advantages of Random Forest:**
- Robust against overfitting  
- Handles high-dimensional features  
- Interpretable predictions  

**Summary:**  
By combining **deep semantic features** and **handcrafted tumor features**, the model predicts survival accurately while considering both tumor appearance and morphology.



# 🔍 Explainable Artificial Intelligence (Grad-CAM)

To improve **interpretability and reliability**, Grad-CAM is employed to identify regions of the MRI image that most influence the model’s predictions.

## 🌟 How Grad-CAM Works
- Grad-CAM analyzes **gradients** flowing through the **final convolutional layer** to generate a **localization map**.  
- **Class Activation Map (LCAM):**  
LCAM = ReLU(Σ α_k * A_k)  
  - A_k = kth feature map of the last convolutional layer  
  - α_k = weight assigned to each feature map  

- **Weight Calculation (α_k):**  
α_k = (1 / Z) * Σ ∂y_c / ∂A_k  
  - y_c = class score  
  - Z = normalization factor over spatial dimensions  

- The resulting **heatmap** is superimposed on the original MRI slice to highlight regions contributing most to the prediction.

---

## 📏 Evaluation Metrics
To measure how well the highlighted regions correspond to actual tumor regions, the following metrics are used:

- **Overlap Ratio:**  
Overlap Ratio = |H ∩ M| / |M|  

- **Intersection over Union (IoU):**  
IoU = |H ∩ M| / |H ∪ M|  

- **Dice Coefficient:**  
Dice = 2 * |H ∩ M| / (|H| + |M|)  

Where:  
- H = binarized Grad-CAM heatmap  
- M = ground truth tumor mask  

**Results:**  
- IoU = 0.467  
- Dice = 0.637  
- Overlap Ratio = 0.553  

---

## ✅ Summary
The Grad-CAM visualization confirms that the model **effectively focuses on clinically relevant tumor regions**, validating the reliability and interpretability of the proposed method.

# 🧠 Brain Tumor Analysis: Working Procedure

A clear visual overview of the **end-to-end workflow** for 2D MRI brain tumor analysis.

---



