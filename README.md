# Real-Time Trash Classification App
![Status](https://img.shields.io/badge/status-complete-brightgreen)
![Model](https://img.shields.io/badge/model-YOLOv8-blue)
![mAP@0.5](https://img.shields.io/badge/mAP@0.5-85.2%25-success)
![Streamlit](https://img.shields.io/badge/UI-Streamlit-orange)
![License](https://img.shields.io/badge/license-MIT-blue)

A web-based app that uses a fine-tuned YOLOv8 object detection model to classify waste into **recyclable** and **non-recyclable** categories in real-time from a webcam or uploaded images.

![Demo](assets/demo.gif)

## Features

-  Real-time classification using YOLOv8
-  Trained on the 60-category [TACO dataset](https://tacodataset.org/)
-  Image augmentation to handle class imbalance
-  Achieved **85.2% mAP@0.5** during validation
-  Upload an image or use a webcam to detect waste items
-  Deployed with Streamlit for easy accessibility

---

##  Model Training

The YOLOv8 model was fine-tuned using the TACO dataset with help from [RoboFlow](https://roboflow.com/). Training was done in Google Colab.

 See: [`yolov8_training.ipynb`](yolov8_training.ipynb)

###  Key Training Details
- Architecture: YOLOv8n (Ultralytics)
- Tools: Roboflow, OpenCV, Ultralytics, Python
- Metrics: 85.2% mAP@0.5
- Techniques: Mosaic & HSV augmentation, weighted sampling, batch balancing

---

## Running the Streamlit App

#### 1. Clone the repo:
  ```bash
  git clone https://github.com/shinieaggarwal72/waste-classification.git
  cd waste-classification
  ```

#### 2. Install dependencies
  ```bash
  pip install -r requiements.txt
  ```

#### 3. Run streamlit app
  ```bash
  streamlit run app/app.py
  ```

