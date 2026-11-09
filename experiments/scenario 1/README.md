# Scenario 1: Dataset Split 70:15:15

## Overview

This experiment evaluates the performance of YOLOv11s and YOLOv12s using a dataset split of 70% training, 15% validation, and 15% testing.

## Dataset Split

| Dataset | Percentage |
|---|---:|
| Training | 70% |
| Validation | 15% |
| Testing | 15% |

## Model Configuration

Both models were trained using the following baseline configuration:

| Parameter | Value |
|---|---|
| Models | YOLOv11s and YOLOv12s |
| Epochs | 50 |
| Batch Size | 16 |
| Image Size | 640 × 640 |
| Optimizer | Ultralytics Auto |
| Pretrained Weights | COCO |
| Random Seeds | 10 runs |

## Experimental Results

The results are organized by model:

- `yolov11s/results.csv`
- `yolov12s/results.csv`

The experiment evaluates model performance using mAP@0.5, mAP@0.5:0.95, Precision, Recall, F1-score, and Accuracy.

## Purpose

## This scenario investigates model performance when 70% of the dataset is allocated for training, with the remaining data divided equally between validation and testing.