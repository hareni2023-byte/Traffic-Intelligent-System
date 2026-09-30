# Traffic Intelligent System

## Project Overview

Traffic Intelligent System is a deep learning-based system designed to detect traffic lights in real-world road scenes and identify their traffic-light states as Red, Yellow, or Green.

The project uses YOLO11n with transfer learning and fine-tuning.

## Current Progress

### Dataset
- Kaggle traffic-light dataset collected
- Dataset downloaded and extracted
- Train, validation, and test sets verified
- YOLO-format annotations verified
- Traffic-light bounding boxes visualized

### Deep Learning Model
- Pretrained YOLO11n model loaded
- YOLO11n architecture inspected
- Transfer learning approach selected
- Layer-freezing strategy planned
- Fine-tuning is in progress

## Technology Stack

- Python
- Google Colab
- YOLO11n
- Ultralytics
- OpenCV
- Deep Learning

## Project Workflow

```text
Road Image / Video
        ↓
YOLO11n
        ↓
Traffic Light Detection
        ↓
Traffic Light State Identification
        ↓
Red / Yellow / Green
