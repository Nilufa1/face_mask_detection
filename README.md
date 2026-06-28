
# Real-Time Face Mask Detection System

A computer vision application built with Python, OpenCV, and TensorFlow/Keras that detects human faces in real-time webcam video feeds and predicts whether individuals are wearing face masks.

## 🚀 Features
* **Real-Time Detection:** Smooth bounding box predictions directly from your webcam stream.
* **Dual Model Pipeline:** Uses a Caffe-based Single Shot Detector (SSD) for reliable face localization and a custom MobileNetV2 architecture for high-accuracy mask categorization.
* **Color-Coded Feedback:** Displays a green bounding box if a mask is detected and a red bounding box if no mask is present.

## 🛠️ Built With
* Python 3.x
* OpenCV (cv2)
* TensorFlow / Keras 3
* MobileNetV2
* Imutils

## 📂 Project Structure
```text
face_mask_detection/
│
├── face_detector/                # (Ignored by Git) Local Caffe model files
│   ├── deploy.prototxt
│   └── res10_300x300_ssd_iter_140000.caffemodel
│
├── mask_detector.h5              # Trained Keras model for mask evaluation
├── detect_mask_video.py          # Core script for real-time video processing
├── train_mask_detector.py         # Model training pipeline script
├── plot.png                      # Training performance graph
├── requirements.txt              # Project dependencies list
└── README.md                     # Project documentation
```

## ⚙️ Setup and Installation

### 1. Clone the Repository
```bash
git clone https://github.com
cd face_mask_detection
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Add Face Detector Weights
Because the face detector model weights are large, they are excluded from Git. You must manually create a `face_detector` folder and download:
* [deploy.prototxt](https://githubusercontent.com)
* [res10_300x300_ssd_iter_140000.caffemodel](https://github.com)

## 🖥️ How to Run
Execute the primary script to initialize your webcam and launch real-time processing:
```bash
python detect_mask_video.py
```
Press `q` on your keyboard to close the live video window safely.

I am proud of myself
