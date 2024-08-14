
# Oriented Object Detection with YOLOv8s-obb

This project involves implementing and evaluating an object detection model that also handles object orientation. The model is trained to detect objects and estimate their orientation in images. This README provides an overview of the project, setup instructions, and usage details.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset Preparation](#dataset-preparation)
3. [Model Implementation](#model-implementation)
4. [Training](#training)
5. [Evaluation](#evaluation)
6. [Visualization](#visualization)
7. [Setup and Usage](#setup-and-usage)
8. [Acknowledgements](#acknowledgements)
9. [References](#references)

## Project Overview

The objective of this project is to implement an object detection model capable of predicting both bounding boxes and orientation angles of objects. The YOLOv8s-obb model is used to achieve this.

## Dataset Preparation

- **Source:** The dataset was annotated using Roboflow, focusing on images with objects such as Tennis courts and Houses.
- **Process:** Images were annotated with bounding boxes and orientation angles. The dataset was divided into training, validation, and test sets.
- **Tools:** Familiarity with Roboflow was leveraged from previous experience to efficiently handle annotation and data preparation.

## Model Implementation

- **Architecture:** YOLOv8s-obb was used, which is modified to predict object orientations along with bounding boxes.
- **Extension:** Adapted YOLO to include orientation prediction capabilities.

## Training

- **Epochs:** Trained for 35 epochs.
- **Results:**
  - **mAP50:** 0.784
  - **mAP50-95:** 0.664
  - **Class Performance:** High accuracy for Tennis courts (0.992) and lower for Houses (0.576).

## Evaluation

- **Metrics:** Evaluated using orientation accuracy, bounding box accuracy, and combined metrics.
- **Results:** Performance metrics indicate successful detection and orientation prediction, with some limitations in angle accuracy.

## Visualization

- **Process:** Predicted bounding boxes and orientation angles were visualized on test images.
- **Conclusion:** The visualization demonstrates the model's capability to handle object detection with orientation, though angle accuracy may be limited due to technology constraints.

## Setup and Usage

1. **Clone the Repository:**

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

3. **Prepare Dataset:**
   - Download and annotate the dataset using Roboflow.
   - Organize images and labels into `train`, `valid`, and `test` directories.

4. **Train the Model:**

    ```bash
    python train.py --data <dataset-path> --weights <pretrained-weights> --epochs <number-of-epochs>
    ```

5. **Evaluate the Model:**

    ```bash
    python evaluate.py --weights <trained-weights> --data <dataset-path>
    ```

6. **Visualize Results:**

    ```bash
    python visualize.py --weights <trained-weights> --data <test-data-path>
    ```

## Acknowledgements

While the visualization successfully demonstrates the model's object detection and orientation capabilities, it's important to note that the accuracy of these angles may be limited due to the constraints of the current technology. Despite this, the code meets the project's requirements and effectively illustrates the model’s functionality.

## References

- [Ultralytics YOLO Documentation](https://docs.ultralytics.com)
- [Roboflow Documentation](https://roboflow.com/docs)
- [Training Custom Dataset YOLOv8-obb](https://alimustoofaa.medium.com/training-custom-dataset-yolov8-obb-oriented-object-detection-9c5bbde99923)
