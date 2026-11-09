# Model Information

## Overview

This project evaluates two YOLO model architectures for bone fracture detection and classification:

- YOLOv11s
- YOLOv12s

Both models use pretrained weights and are fine-tuned on the annotated X-ray dataset.

## Model Architecture

| Model | Description |
|---|---|
| YOLOv11s | Small variant of YOLOv11 |
| YOLOv12s | Small variant of YOLOv12 |

## Pretrained Weights

The pretrained weights used in this project are:

- `yolo11s.pt`
- `yolo12s.pt`

The models were initialized with pretrained weights and trained on the fracture dataset.

## Best Performing Configuration

The best overall configuration in the research comparison was YOLOv12s with Scenario 3 (80:10:10).

| Metric | Result |
|---|---:|
| mAP@0.5 | 88.76% |
| Precision | 84.70% |
| Recall | 83.23% |
| F1-score | 83.95% |
| Accuracy | 97.72% |

## Trained Weights

The trained model checkpoint files (`best.pt`) are not included in this repository.

The pretrained weights can be obtained through the Ultralytics framework. Trained checkpoints may be shared separately if available.

## Notes This repository focuses on the research workflow, experimental configurations, evaluation results, and visual outputs rather than distributing large model checkpoint files.