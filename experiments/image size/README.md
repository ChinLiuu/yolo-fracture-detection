# Image Size Experiment: YOLOv12s Scenario 3

## Overview

This experiment investigates the effect of input image size on the performance and computational time of YOLOv12s trained using Scenario 3 (80:10:10).

Three input image sizes were evaluated:

- 416 × 416
- 640 × 640
- 832 × 832

## Experimental Configuration

| Parameter | Value |
|---|---|
| Model | YOLOv12s |
| Dataset Split | Scenario 3 (80:10:10) |
| Epochs | 50 |
| Batch Size | 16 |
| Input Image Sizes | 416, 640, 832 |

## Experimental Results

| Image Size | mAP@0.5 | Accuracy | Computation Time |
|---|---:|---:|---:|
| 416 × 416 | 86.10% | 97.3% | ~800 seconds |
| 640 × 640 | 86.30% | 97.0% | ~1,650 seconds |
| 832 × 832 | 87.58% | 97.1% | ~3,310 seconds |

## Analysis

The 832 × 832 input size achieved the highest mAP@0.5 among the three tested image sizes.

The 416 × 416 input size achieved the highest accuracy and required the shortest computation time.

The 640 × 640 input size provided a practical balance between detection performance and computational cost.

## Conclusion

Although the 832 × 832 input size achieved the highest mAP@0.5, the 640 × 640 input size was considered a practical choice when balancing performance and computational requirements.

## Results File

## The `results.csv` file contains the image size experiment results reported in this project.