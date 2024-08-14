Oriented Object Detection with YOLOv8s-obb
This project involves implementing and evaluating an object detection model that also handles object orientation. The model is trained to detect objects and estimate their orientation in images. This README provides an overview of the project, setup instructions, and usage details.

Table of Contents
Project Overview
Dataset Preparation
Model Implementation
Training
Evaluation
Visualization
Setup and Usage
Acknowledgements
References
Project Overview
The objective of this project is to implement an object detection model capable of predicting both bounding boxes and orientation angles of objects. The YOLOv8s-obb model is used to achieve this.

Dataset Preparation
Source: The dataset was annotated using Roboflow, focusing on images with objects such as Tennis courts and Houses.
Process: Images were annotated with bounding boxes and orientation angles. The dataset was divided into training, validation, and test sets.
Tools: Familiarity with Roboflow was leveraged from previous experience to efficiently handle annotation and data preparation.
Model Implementation
Architecture: YOLOv8s-obb was used, which is modified to predict object orientations along with bounding boxes.
Extension: Adapted YOLO to include orientation prediction capabilities.
Training
Epochs: Trained for 35 epochs.
Results:
mAP50: 0.784
mAP50-95: 0.664
Class Performance: High accuracy for Tennis courts (0.992) and lower for Houses (0.576).
Evaluation
Metrics: Evaluated using orientation accuracy, bounding box accuracy, and combined metrics.
Results: Performance metrics indicate successful detection and orientation prediction, with some limitations in angle accuracy.
Visualization
Process: Predicted bounding boxes and orientation angles were visualized on test images.
Conclusion: The visualization demonstrates the model's capability to handle object detection with orientation, though angle accuracy may be limited due to technology constraints.
Setup and Usage
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd <repository-directory>
Install Dependencies:

bash
Copy code
pip install -r requirements.txt
Prepare Dataset:

Download and annotate the dataset using Roboflow.
Organize images and labels into train, valid, and test directories.
Train the Model:

bash
Copy code
python train.py --data <dataset-path> --weights <pretrained-weights> --epochs <number-of-epochs>
Evaluate the Model:

bash
Copy code
python evaluate.py --weights <trained-weights> --data <dataset-path>
Visualize Results:

bash
Copy code
python visualize.py --weights <trained-weights> --data <test-data-path>
Acknowledgements
While the visualization successfully demonstrates the model's object detection and orientation capabilities, it's important to note that the accuracy of these angles may be limited due to the constraints of the current technology. Despite this, the code meets the project's requirements and effectively illustrates the model’s functionality.

References
Ultralytics YOLO Documentation
Roboflow Documentation
Training Custom Dataset YOLOv8-obb
