# Scenario 3: Dataset Split 80:10:10

## Overview

This experiment evaluates YOLOv11s and YOLOv12s using a dataset split of 80% training, 10% validation, and 10% testing.

This scenario achieved the best overall performance in the research comparison.

## Dataset Split

| Dataset | Percentage |
|---|---:|
| Training | 80% |
| Validation | 10% |
| Testing | 10% |

## Dataset Distribution

The Scenario 3 split contained 2,367 images in total.

| Dataset | Number of Images |
|---|---:|
| Training | 1,893 |
| Validation | 237 |
| Testing | 237 |

## Model Configuration

| Parameter | Value |
|---|---|
| Models | YOLOv11s and YOLOv12s |
| Epochs | 50 |
| Batch Size | 16 |
| Image Size | 640 × 640 |
| Optimizer | Ultralytics Auto |
| Pretrained Weights | COCO |

## Experimental Results

The results are organized by model:

- `yolov11s/results.csv`
- `yolov12s/results.csv`

The experiment evaluates model performance using mAP@0.5, mAP@0.5:0.95, Precision, Recall, F1-score, and Accuracy.

## Best Overall Model

YOLOv12s with Scenario 3 achieved the following reported results:

| Metric | Result |
|---|---:|
| mAP@0.5 | 88.76% |
| Precision | 84.70% |
| Recall | 83.23% |
| F1-score | 83.95% |
| Accuracy | 97.72% |

## Purpose = This scenario investigates the effect of allocating a larger proportion of the dataset to training while maintaining separate validation and testing sets.