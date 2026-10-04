# Trained Models

This folder contains the trained deep learning models used in the
Traffic Intelligent System.

## YOLO11n Traffic Light Detector

**File:** `traffic_light_detector.pt`

YOLO11n detects traffic lights in road images.

### Validation Results

- Precision: 92.95%
- Recall: 88.81%
- mAP@50: 93.24%
- mAP@50-95: 49.03%

## ResNet18 Traffic Light Color Classifier

**File:** `traffic_light_color_classifier.pth`

ResNet18 classifies detected traffic-light crops into:

- Red
- Yellow
- Green

### Validation Result

- Accuracy: 100%

> Note: The validation set contains only 7 yellow samples, so the
> yellow-class result should be interpreted cautiously.

## Pipeline

YOLO11n detects the traffic light first.

The detected region is cropped.

ResNet18 then predicts the traffic-light color.
