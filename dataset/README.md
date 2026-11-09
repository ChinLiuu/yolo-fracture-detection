# Dataset Information

## Overview

This project uses X-ray images to identify and classify two types of bone fractures: Simple and Comminuted fractures.

The dataset was collected from two sources:

- Kaggle Bone Fracture Dataset
- Bone Break Classifier Dataset

After dataset selection and annotation, a total of **2,367 X-ray images** were used in the research.

## Dataset Classes

| Class | Number of Images |
|---|---:|
| Simple | 1,243 |
| Comminuted | 1,150 |
| **Total** | **2,367** |

## Annotation

The images were annotated using Roboflow in YOLO format.

Each annotation contains a bounding box and a class label corresponding to the fracture type.

## Preprocessing

- Images were standardized to 640 × 640 pixels during baseline model training.
- Dataset annotations were prepared in YOLO format.
- The dataset was divided into training, validation, and testing sets according to three experimental scenarios.

## Dataset Availability

The dataset files are not included in this repository.

Please refer to the original dataset sources and their respective licenses and usage conditions.

## Notes

The dataset was used exclusively for the research and experiments described in this project.