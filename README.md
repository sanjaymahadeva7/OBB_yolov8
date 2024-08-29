# **YOLOv8s-OBB for Detecting Houses and Tennis Courts**

## **Project Overview**

This project leverages the **YOLOv8s-OBB** model to detect and classify **houses** and **tennis courts** in images. The dataset was carefully annotated and preprocessed using **Roboflow** to optimize detection accuracy. This project demonstrates the power of Object-Oriented Bounding Boxes (OBB) in enhancing object detection, especially for objects with irregular orientations.

## **Table of Contents**

1. [Project Structure](#project-structure)
2. [Data Preparation](#data-preparation)
3. [Model Training](#model-training)
4. [Results](#results)
5. [Key Highlights](#key-highlights)
6. [How to Use](#how-to-use)
7. [Acknowledgments](#acknowledgments)
8. [Contact](#contact)

## **Project Structure**

```
.
├── datasets/
│   ├── train/
│   ├── test/
│   └── valid/
├── runs/
│   ├── obb/
│       ├── train/
│       └── val/
├── notebooks/
│   ├── training_notebook.ipynb
├── README.md
└── requirements.txt
```


## **Data Preparation**

The dataset used in this project was prepared and annotated by myself, using **Roboflow** for preprocessing. It includes:

- **Annotations:** Each image was annotated with Object-Oriented Bounding Boxes (OBBs) to enhance detection accuracy for rotated or skewed objects.
- **Classes:** The dataset contains two classes: `houses` and `tennis_courts`.
- **Normalization:** Images and labels were normalized and resized to fit the input size of the YOLOv8s-OBB model.

## **Model Training**

The YOLOv8s-OBB model was fine-tuned using the prepared dataset:

- **Model:** YOLOv8s-OBB.
- **Training:** The model was trained for 35 epochs with a batch size of 8.
- **Optimization:** Used adaptive learning rates and data augmentation for better generalization.

## **Results**

The model successfully detected and classified houses and tennis courts in the test images. Here are some examples:

![Example 1](./runs/obb/val/sample1.jpg)
![Example 2](./runs/obb/val/sample2.jpg)

## **Key Highlights**

- **Object-Oriented Bounding Boxes (OBBs):** These bounding boxes allow for more precise detection of objects that are not perfectly aligned with the image axes.
- **Applications:** The use of OBBs can be extended to various fields such as urban planning, disaster management, and aerial imagery analysis.

## **How to Use**

1. **Inference:**
   To run inference on new images, follow the steps in the `training_notebook.ipynb` notebook.

2. **Evaluation:**
   Evaluate the model using the test dataset provided in the `datasets/test/` directory.

3. **Customization:**
   You can retrain the model with your own dataset by following the steps in the `training_notebook.ipynb`.

## **Acknowledgments**

Special thanks to **Roboflow** for providing an excellent platform for dataset preparation and to the **YOLO** community for their continuous contributions to object detection research.

## **Contact**

For any inquiries or collaboration opportunities, feel free to reach out to me:

- **Email:** [sanjaykabaddi5858@gmail.com](mailto:sanjaykabaddi5858@gmail.com)
