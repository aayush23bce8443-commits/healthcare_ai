
---

## 🖼 Image Specifications

- File format: `.tif`
- 3-channel MRI images
- Multi-sequence format

### Standard Channel Order

1. Pre-contrast
2. FLAIR
3. Post-contrast

---

## ⚠️ Missing Sequence Handling

- 101 cases → All 3 sequences available
- 9 cases → Post-contrast missing
- 6 cases → Pre-contrast missing

To maintain consistency:

> Missing sequences are replaced with the FLAIR sequence.

Thus, all images are standardized as 3-channel images.

---

## 🎯 Segmentation Masks

- Format: `.tif`
- Single-channel binary mask
- Pixel values:
  - `1` → Tumor (FLAIR abnormality)
  - `0` → Background

Masks segment abnormalities present in the FLAIR sequence.

---

## 📁 Dataset Organization

The dataset is structured into 110 folders named after case IDs.

Each folder contains:

- MRI image slices
- Corresponding mask images

### Naming Convention

MRI Image:

TCGA_<institution-code>_<patient-id>_<slice-number>.tif

Mask Image:

TCGA_<institution-code>_<patient-id>_<slice-number>_mask.tif

---

## 📥 Full Dataset & Code Access

All dataset files and additional resources are hosted on Google Drive:

🔗 **Google Drive Folder:**
https://drive.google.com/drive/folders/1boKcONk7EAoKmFVshWo3DrElXsTO9Pis?dmr=1&ec=wgc-drive-%5Bmodule%5D-goto

---

## 📘 Repository Contents

This GitHub repository contains:

- Main Jupyter Notebook (`.ipynb`) file
- Project documentation (`README.md`)

The notebook includes:

- Data preprocessing
- Model architecture
- Training pipeline
- Evaluation
- Visualization of segmentation results

---

## 🧪 Applications

This dataset and notebook can be used for:

- Brain tumor classification
- Tumor segmentation (FLAIR abnormality)
- Deep learning research
- Transfer learning experiments
- Medical image analysis

---

## 📌 Note

The dataset is not stored directly in this repository due to size limitations.  
Please download the dataset from the Google Drive link before running the notebook.

---