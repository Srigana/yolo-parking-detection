1. Project Title & Group Members
YOLO-Based Vehicle Detection and Counting System Using Flask

Group Members:
Eshika Sanjana Konyala
Mazik Fernandes
Sowmya Sri Regu
Srigana Pulikantham
Tejesh Annavarapu

2. Overview
This project provides a web-based application that detects and counts vehicles in an image using YOLOv5 and YOLOv8 object-detection models.
A Flask interface allows a user to upload an image, processes it using both models, and returns:

Detected objects with bounding boxes (YOLOv5 + YOLOv8)
Vehicle-count results
Side-by-side visual comparison of detections

This system is useful for automated parking analysis, traffic monitoring, surveillance pipelines, and remote-sensing scenarios where fast, accurate detection is required.

3. Setup Instructions
Prerequisites
Install Python 3.8–3.11.
Install Dependencies
pip install flask ultralytics opencv-python torch torchvision numpy
If YOLOv5 dependencies are missing (for detect.py):
pip install matplotlib pillow tqdm

4. Execution Steps

Run the Flask App
python app.py

Open in Browser
http://127.0.0.1:5000/

Using the Application
Upload an image containing vehicles.

The system:

Runs YOLOv5 using detect.py
Runs YOLOv8 via Ultralytics
Processes outputs concurrently using threads
Results are displayed on result.html:
YOLOv5 detection image
YOLOv8 detection image
Vehicle count from YOLOv5
YOLOv8 estimated count

6. Software Requirements
Operating Systems
Windows 10/11
macOS
Linux (Ubuntu recommended)
Python Version
Python 3.8 – 3.11

Frameworks / Libraries
Flask
PyTorch
Ultralytics YOLOv8
OpenCV
NumPy
shutil, subprocess, threading (Python standard libraries)

Optional
CUDA-capable GPU for faster YOLOv8 inference