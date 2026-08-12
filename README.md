# Vehicle Detection and Video Analytics Using YOLO11

## Project Overview

This project implements a complete computer vision pipeline using Ultralytics YOLO11.

The system performs:

- Object Detection
- Instance Segmentation
- Object Tracking
- Object Counting
- Model Training
- Model Evaluation

## Dataset

Vehicle Detection Dataset from Roboflow.

Classes:

- Car
- Bus
- Truck
- Motorbike

Dataset split:

- Training: 800 images
- Validation: 100 images
- Testing: 100 images

## Technologies

- Python
- Google Colab
- Ultralytics YOLO11
- OpenCV
- Roboflow

## Training Configuration

- Model: YOLO11n
- Epochs: 10
- Image size: 640
- Batch size: 16

## Results

| Metric | Value |
| --- | --- |
| Precision | 0.874 |
| Recall | 0.789 |
| mAP50 | 0.880 |
| mAP50-95 | 0.681 |

## Video Analytics

Implemented features:

- Tracking
- Person counting

## Files

- best.pt
- training results
- evaluation results
- tracking videos

## SDAIA Academy Attribution

This project was completed as part of the Computer Vision for Developers with Ultralytics training program delivered by SDAIA Academy.

SDAIA Academy:
https://github.com/SDAIAAcademy

## Author

Nouf Alrubayyi
