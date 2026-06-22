# 🌱 Crop and Weed Detection using YOLOv8

## 📌 Project Overview

This project implements a Computer Vision-based Crop and Weed Detection system using the YOLOv8 object detection framework.

The objective is to automatically identify and localize crops and weeds in agricultural field images, helping farmers monitor weed infestation and improve precision farming practices.

The system uses Deep Learning and Object Detection techniques to classify agricultural objects and generate bounding boxes around detected crops and weeds.

This project was developed as part of the UpskillCampus Internship Program.

---

## 🎯 Problem Statement

Manual weed detection in agricultural fields is time-consuming, labor-intensive, and prone to errors.

An automated detection system can:

* Reduce human effort
* Improve weed management
* Support precision agriculture
* Minimize unnecessary herbicide usage
* Increase crop productivity

---

## 🚀 Objectives

* Detect crops and weeds from field images
* Train a custom YOLOv8 object detection model
* Evaluate model performance using industry-standard metrics
* Visualize detections on unseen images

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Libraries & Frameworks

* YOLOv8 (Ultralytics)
* OpenCV
* NumPy
* PyYAML
* Matplotlib

### Development Environment

* Google Colab

---

## 📂 Dataset Information

The dataset contains agricultural field images with annotations for:

* Crop
* Weed

Dataset Structure:

```text
images/
├── train/
├── val/

labels/
├── train/
├── val/
```

Annotation Format:

```text
class_id x_center y_center width height
```

YOLO format annotation files were used.

---

## 🔍 Methodology

### Step 1: Dataset Preparation

* Extract dataset
* Organize images and labels
* Create train-validation split

### Step 2: Dataset Configuration

Create YOLO dataset configuration file:

```yaml
path: /content/data
train: images/train
val: images/val

nc: 2

names:
  - crop
  - weed
```

### Step 3: Model Training

YOLOv8 Nano model was used:

```python
model = YOLO("yolov8n.pt")
```

Training Parameters:

* Epochs: 50
* Image Size: 512
* Batch Size: 16

### Step 4: Model Evaluation

Performance evaluated using:

* Precision
* Recall
* mAP@50
* mAP@50-95

### Step 5: Prediction

The trained model predicts:

* Crop locations
* Weed locations
* Bounding boxes
* Confidence scores

---

## 📊 Results

Training Configuration:

| Parameter  | Value   |
| ---------- | ------- |
| Model      | YOLOv8n |
| Epochs     | 50      |
| Batch Size | 16      |
| Image Size | 512     |
| Classes    | 2       |

Metrics:

* Precision
* Recall
* mAP@50
* mAP@50-95

The model successfully identified crops and weeds in validation images with satisfactory detection accuracy.

---

## 📈 Sample Workflow

```text
Input Image
      ↓
YOLOv8 Model
      ↓
Object Detection
      ↓
Crop / Weed Classification
      ↓
Bounding Box Generation
      ↓
Output Visualization
```

---

## 🌾 Applications

* Precision Agriculture
* Smart Farming
* Weed Monitoring
* Agricultural Automation
* Crop Health Analysis

---

## 🔮 Future Improvements

* Real-time drone-based monitoring
* Mobile application integration
* AI-powered agricultural recommendations
* Multi-class crop identification
* Weed density analytics dashboard

---

## 📁 Repository Contents

```text
upskillCampus/
│
├── Crop_Weed_Detection.ipynb
├── README.md
├── Report.pdf
├── dataset.yaml
├── best.pt
└── outputs/
```

---

## 👩‍💻 Author

Shravani R. Patil

Computer Engineering Student

UpskillCampus Internship Program

---

## 📜 License

This project is developed for educational and internship purposes.

