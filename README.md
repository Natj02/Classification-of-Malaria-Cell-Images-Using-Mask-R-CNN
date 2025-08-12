# Classification of Malaria Cell Images Using Mask R-CNN

## Overview
This project implements **Mask R-CNN** for detecting and classifying **infected vs. uninfected malaria cell images**.  
By combining object detection with pixel-level segmentation, the model provides a highly detailed approach for malaria diagnosis in blood smear images.

---

## Dataset
The dataset used is the **Malaria Cell Images Dataset** from [Kaggle](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria), originally from the **NIH website**.

- **Total images available:** 27,558  
- **Classes:**  
  - Infected red blood cells  
  - Uninfected red blood cells  

For this project:
- **Selected images:** 2,000 (1,000 infected, 1,000 uninfected)  
- **Split:**
  - 1,600 images for training
  - 400 images for validation
- **Annotation Tool:** [VGG Image Annotator (VIA)](http://www.robots.ox.ac.uk/~vgg/software/via/)  
- **Annotation shapes:** Polygon and ellipse for accurate outlining of cell structures.

---

## Model Architecture
We use **Mask R-CNN**, an advanced instance segmentation model that extends Faster R-CNN by adding a branch for predicting **segmentation masks** alongside bounding box detection.

**Key features:**
- **Region Proposal Network (RPN):** Generates candidate regions of interest (RoIs).  
- **RoI Align:** Preserves spatial accuracy and mitigates misalignment issues from pooling operations.  
- **Outputs:** Bounding box recognition, class prediction, and pixel-level segmentation masks.  
- **Advantage:** Provides both detection and fine-grained shape segmentation of infected cells.

---
