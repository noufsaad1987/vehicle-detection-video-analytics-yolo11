# Vehicle Detection and Video Analytics Using YOLO11

## Project Overview

This project was developed as part of the **Computer Vision for Developers with Ultralytics** training program delivered by **SDAIA Academy**.

The project implements an end-to-end computer vision pipeline using **Ultralytics YOLO11** to analyze vehicles in images and videos.

The system performs multiple computer vision tasks, including object detection, instance segmentation, object tracking, object counting, model training, and model evaluation.

---

## Problem Statement

Monitoring vehicles manually in traffic videos is time-consuming and inefficient.

This project provides an automated solution that can:

- Detect vehicles automatically.
- Track moving objects in videos.
- Count objects crossing a predefined region.
- Train a custom model using a real-world dataset.
- Evaluate model performance using standard computer vision metrics.

---

## Project Tasks

### 1. Object Detection

A YOLO11 object detection model was used to identify different objects in images and videos.

Implemented using:

- `model.predict()`

---

### 2. Instance Segmentation

A segmentation model (`yolo11n-seg.pt`) was used to identify the exact boundaries of detected objects.

Implemented using:

- `model.predict()`
- `yolo11n-seg.pt`

---

### 3. Object Tracking

Vehicle movement was tracked across video frames.

Implemented using:

- `model.track()`
- `BoT-SORT Tracker`

---

### 4. Object Counting

A counting line was defined to count objects moving across a selected region in the video.

Implemented using:

- `ObjectCounter`

---

### 5. Custom Training

A custom YOLO11 model was trained using a real-world dataset from Roboflow.

Training configuration:

| Parameter | Value |
| --- | --- |
| Model | YOLO11n |
| Epochs | 10 |
| Image Size | 640 |
| Batch Size | 16 |

---

## Dataset

**Dataset source:**

Roboflow Universe

**Dataset name:**

Vehicle Detection

**Classes:**

- Car
- Bus
- Truck
- Motorbike

**Dataset split:**

| Dataset | Images |
| --- | --- |
| Training | 800 |
| Validation | 100 |
| Testing | 100 |

---

## Model Evaluation

| Metric | Value |
| --- | --- |
| Precision | 0.874 |
| Recall | 0.789 |
| mAP50 | 0.880 |
| mAP50-95 | 0.681 |

### Class Performance

| Class | mAP50 |
| --- | --- |
| Car | 0.945 |
| Bus | 0.917 |
| Truck | 0.854 |
| Motorbike | 0.806 |

---

## Technologies Used

- Python
- Google Colab
- Ultralytics YOLO11
- OpenCV
- Roboflow

---
## Technical Documentation

### Pipeline Overview

1. Object Detection using YOLO11n.
2. Instance Segmentation using YOLO11n-seg.
3. Object Tracking using BoT-SORT.
4. Object Counting using ObjectCounter.
5. Custom model training using a Roboflow dataset.
6. Model evaluation using Precision, Recall, mAP50, and mAP50-95.

### Training Details

- Dataset source: Roboflow Universe
- Training epochs: 10
- Image size: 640
- Batch size: 16

  ---
## Repository Structure

```
.
├── README.md
└── Vehicle_Detection_YOLO11.ipynb
```

---

## How to Run the Project

### Install dependencies

```bash
pip install ultralytics
pip install roboflow
```

### Run object detection

```bash
yolo predict model=yolo11n.pt source=image.jpg
```

### Run object tracking

```bash
yolo track model=yolo11n.pt source=video.mp4
```

### Train the model

```bash
yolo train model=yolo11n.pt data=data.yaml epochs=10 imgsz=640
```

### Evaluate the model

```bash
yolo val model=best.pt data=data.yaml
```

---

## SDAIA Academy Attribution

This project was completed as part of the **Computer Vision for Developers with Ultralytics** training program delivered by **SDAIA Academy**.

SDAIA Academy:

https://github.com/SDAIAAcademy

---

## Author

**Nouf Alrubayyi**

Lecturer, Computer Science Department

AlMaarefa University
