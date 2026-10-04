readme = """
# Traffic Intelligent System

A deep learning-based traffic intelligent system that detects traffic lights
in road scenes and identifies their current state as Red, Yellow, or Green.

## System Architecture

Input Road Image
        |
        v
YOLO11n Traffic Light Detection
        |
        v
Traffic Light Bounding Box
        |
        v
Crop Detected Traffic Light
        |
        v
ResNet18 Color Classification
        |
        v
RED / YELLOW / GREEN

## Technologies Used

- Python
- Google Colab
- PyTorch
- Torchvision
- Ultralytics YOLO11n
- ResNet18
- OpenCV / PIL
- Matplotlib
- Scikit-learn

## Dataset

### Traffic Light Detection

Dataset:
S2TLD (Small Traffic Light Dataset)

- Training images: 1022
- Validation images: 200
- Validation traffic-light instances: 402
- Original annotations: XML
- Converted annotations: YOLO format
- Detector classes: 1 (traffic_light)

### Traffic Light Color Classification

Classes:

- Red
- Yellow
- Green

The classifier was trained using cropped traffic-light images
generated from the S2TLD annotations.

## YOLO11n Results

- Precision: 92.95%
- Recall: 88.81%
- mAP@50: 93.24%
- mAP@50-95: 49.03%

## ResNet18 Results

Validation images: 352

- Accuracy: 100%
- Green precision: 100%
- Red precision: 100%
- Yellow precision: 100%

Note: The validation set contains only 7 yellow samples,
so the yellow-class result should be interpreted with caution.

## End-to-End Pipeline

The complete system was tested on road images.

The system successfully:

1. Detects traffic lights using YOLO11n.
2. Extracts the detected traffic-light region.
3. Classifies the traffic-light color using ResNet18.
4. Displays the bounding box, predicted color, and confidence.

## Project Status

The core detection and color-classification pipeline is working.

Future improvements include:

- Larger and more balanced color-classification dataset
- More yellow-light samples
- Handling additional traffic-light states such as off/wait_on
- Testing on larger real-world image and video datasets
- Real-time video inference
"""

readme_path = "/content/traffic_intelligent_system/README.md"

with open(readme_path, "w") as f:
    f.write(readme)

print("README.md created successfully!")
print(readme_path)
