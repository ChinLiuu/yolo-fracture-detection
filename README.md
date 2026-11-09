# YOLO-Based Bone Fracture Detection and Classification

A deep learning project for detecting and classifying bone fractures in X-ray images using YOLOv11s and YOLOv12s.

## Overview

Bone fractures can vary in their structural patterns. This project applies object detection techniques to identify and classify two types of bone fractures from X-ray images:

- **Simple Fracture:** A fracture that produces two bone fragments.
- **Comminuted Fracture:** A fracture that produces more than two bone fragments.

The system uses YOLO-based object detection to locate fracture regions through bounding boxes and classify the detected fractures.

## Research Objectives

The main objectives of this project are:

1. Develop a YOLO-based system for bone fracture detection and classification.
2. Compare the performance of YOLOv11s and YOLOv12s.
3. Evaluate different dataset splitting scenarios.
4. Analyze the effect of input image sizes on model performance.

## Dataset

The dataset consists of **2,367 annotated X-ray images** from two bone fracture dataset sources:

- Kaggle Bone Fracture Dataset
- Bone Break Classifier Dataset

### Dataset Classes

| Class | Number of Images |
|---|---:|
| Simple Fracture | 1,243 |
| Comminuted Fracture | 1,150 |
| **Total** | **2,367** |

The dataset was annotated using Roboflow in YOLO format.

## Methodology

The research workflow consists of the following stages:

1. Dataset collection and selection.
2. Image annotation using Roboflow.
3. Dataset splitting into training, validation, and testing sets.
4. Model training using YOLOv11s and YOLOv12s.
5. Model evaluation and performance comparison.
6. Input image size experiments.

## Models

Two YOLO architectures were evaluated:

- YOLOv11s
- YOLOv12s

Both models used pretrained weights and were fine-tuned on the fracture X-ray dataset.

### Training Configuration

| Parameter | Configuration |
|---|---|
| Epochs | 50 |
| Batch Size | 16 |
| Baseline Image Size | 640 × 640 |
| Optimizer | Ultralytics Auto |
| Pretrained Weights | COCO |
| Random Seeds | 10 runs |
| GPU | NVIDIA Tesla T4 |

## Experimental Scenarios

Three dataset splitting scenarios were evaluated:

| Scenario | Training | Validation | Testing |
|---|---:|---:|---:|
| Scenario 1 | 70% | 15% | 15% |
| Scenario 2 | 70% | 20% | 10% |
| Scenario 3 | 80% | 10% | 10% |

Both YOLOv11s and YOLOv12s were evaluated across all three scenarios.

## Evaluation Metrics

Model performance was evaluated using:

- Mean Average Precision at IoU 0.5 (mAP@0.5)
- mAP@0.5:0.95
- Precision
- Recall
- F1-score
- Accuracy

## Research Results

The best overall experimental configuration was **YOLOv12s with Scenario 3 (80:10:10)**.

| Metric | Result |
|---|---:|
| mAP@0.5 | 88.76% |
| Precision | 84.70% |
| Recall | 83.23% |
| F1-score | 83.95% |
| Accuracy | 97.72% |

The scenario comparison results represent the average of 10 training runs with different random seeds.

## Image Size Experiment

The YOLOv12s model trained using Scenario 3 was further evaluated with three input image sizes.

| Input Image Size | mAP@0.5 | Accuracy | Computation Time |
|---|---:|---:|---:|
| 416 × 416 | 86.10% | 97.3% | ~800 seconds |
| 640 × 640 | 86.30% | 97.0% | ~1,650 seconds |
| 832 × 832 | 87.58% | 97.1% | ~3,310 seconds |

The 832 × 832 input size achieved the highest mAP@0.5, while 640 × 640 provided a practical balance between detection performance and computational cost.

## Technologies Used

- Python
- Ultralytics YOLO
- Google Colab
- Roboflow
- OpenCV
- NumPy
- Pandas
- Matplotlib

## Repository Structure

```text
yolo-fracture-detection/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── YOLOHELENA.ipynb
│
├── dataset/
│   └── README.md
│
├── experiments/
│   ├── scenario_1/
│   ├── scenario_2/
│   ├── scenario_3/
│   └── image_size/
│
├── results/
│   ├── scenario_comparison.csv
│   └── figures/
│
└── models/
    └── README.md
```

## Limitations

- The system focuses on two fracture types: Simple and Comminuted.
- The research uses X-ray image information only.
- The experiments are limited to YOLOv11s and YOLOv12s.
- The system focuses on fracture detection and classification.

## Future Improvements

Potential future development includes:

- Expanding the number of fracture classes.
- Evaluating additional YOLO architectures.
- Improving dataset diversity.
- Exploring further model optimization.

## Author

**Helena Alycia Liu**

Computer Science Graduate

Nusa Cendana University

## Acknowledgment

This project is based on my undergraduate thesis research on YOLO-based bone fracture identification and classification using X-ray images.