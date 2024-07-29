# Detection Project with YOLOv10

This project aims to detect three specific classes: Wallet, Airpods, and Phone using the YOLOv10 model. The project includes training the model, analyzing the results with a confusion matrix and metrics curves, and testing the model's performance on a video file.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Analysis Results](#analysis)
- [Testing](#testing)

## Project Overview

The goal of this project is to develop an object detection system that can accurately identify Wallets, Airpods, and Phones in images and video footage. The project leverages the YOLOv10 model for detection, and the performance is evaluated using various metrics. The project involves the following steps:

1. **Dataset Preparation**: Collecting and annotating images for the three classes using webcam.
2. **Model Training**: Training the YOLOv10 model on the prepared dataset ( There is 6 versions for my project I used the small version "yolov10s")
3. **Result Analysis**: Evaluating the model's performance using a confusion matrix and metrics curves.
4. **Video Testing**: Using the trained model ( You can find it in the folder run/detect/train/weights/best.pt ) to detect the three classes in a video file and assessing its performance.

## Dataset

The dataset used for this project includes annotated images of Wallets, Airpods, and Phones. The annotations are done using Roboflow ( https://roboflow.com/)

## Analyzing Results
After training, analyze the model's performance:

1. **Confusion Matrix:**

Generate the confusion matrix to understand the classification performance across different classes.

2. **Metrics Curves:**

Plot metrics such as Precision-Recall curves, F1 scores, and Loss curves to evaluate the model's training and validation performance.

## Testing
To test the trained model on a video file, you can run the inference script which will process the video and output the detections for Wallets, AirPods, and Phones.
```bash
%cd {HOME}
!yolo task=detect mode=predict conf=0.25 save=True model=/content/runs/detect/train/weights/best.pt source=/content/video.mp4

