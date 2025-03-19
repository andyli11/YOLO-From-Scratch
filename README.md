# 👁️ YOLO-Based Single-Stage Object Detector

Welcome to the YOLO (You Only Look Once) Single-Stage Object Detector project! 🚀  
This repository contains an implementation of a real-time object detection system built using **YOLO (v1 & v2)** principles and trained on the **PASCAL VOC 2007 dataset**. The objective is to detect objects in images efficiently while evaluating performance using mean Average Precision (mAP).

---

## 📌 Project Overview
This project involves:
- **Implementing a YOLO-based single-stage object detector** 🔍
- **Training and evaluating the model using the PASCAL VOC 2007 dataset** 📊
- **Using mean Average Precision (mAP) for performance assessment** 🎯
- **Implementing Non-Maximum Suppression (NMS) for filtering redundant detections** ✂️
- **Utilizing PyTorch for deep learning model training and inference** ⚡
- **Preprocessing images and annotations with a custom DataLoader** 🗂️  

![image](https://github.com/user-attachments/assets/06d97c07-cf71-4cb9-894e-18a691622458)

## 📌 YOLO Architecture Overview

The YOLO-based **single-stage object detector** processes an input image through a **convolutional neural network (CNN)**, extracting feature maps and predicting object locations. The architecture follows these key stages:

### **1. Feature Extraction**
- The input image (e.g., **300×300 pixels**) is processed through a **deep convolutional network**.
- The CNN extracts meaningful features using **convolutional layers**, reducing the spatial dimensions while increasing the depth (channels).

### **2. Image Feature Maps**
- The extracted features are converted into **feature maps** of reduced spatial size (**e.g., 19×19, 512 channels**).
- These maps retain important object-related information while compressing unnecessary details.

### **3. Auxiliary Convolutions**
- Additional **convolutional layers** refine the extracted features.
- These layers help capture contextual relationships and enhance object detection capabilities.

### **4. Prediction Convolutions & Anchor Boxes**
- The final feature maps are processed through specialized **prediction convolutions**.
- The model applies **k anchor boxes** (predefined bounding box shapes) at different locations on the feature maps.
- Each anchor predicts:
  - **Bounding box coordinates** (x, y, width, height)
  - **Object confidence scores**
  - **Class probabilities**

### **5. Final Object Detections**
- The output consists of **multiple bounding boxes** predicted across different anchor locations.
- A **Non-Maximum Suppression (NMS) algorithm** is applied to filter out overlapping and low-confidence detections.
- The final output is a set of **accurate bounding boxes** with class labels and confidence scores.

🔹 This **end-to-end architecture** allows **real-time object detection**, making YOLO one of the fastest object detection models available. 🚀


![image](https://github.com/user-attachments/assets/bce2cdee-77aa-41ea-9553-87697b363076)
