# 🚀 Containerized Parking Surveillance Pipeline: YOLOv5 vs. YOLOv8

[![Docker](https://img.shields.io/badge/Docker-Enabled-blue?logo=docker)](https://www.docker.com/)
[![Flask](https://img.shields.io/badge/Framework-Flask-lightgrey?logo=flask)](https://flask.palletsprojects.com/)
[![Python](https://img.shields.io/badge/Python-3.10-3776AB?logo=python)](https://www.python.org/)

A containerized computer vision web application that performs concurrent vehicle detection using both YOLOv5 and YOLOv8 models. This project benchmarks performance and accuracy across different versions of the YOLO architecture.

## 🌟 Key Features
- **Concurrent Inference:** Utilizes Python `threading` to run both detection models simultaneously, optimizing API response time.
- **Dockerized Environment:** Fully containerized with system-level dependencies (`libgl1`, `libglib2.0-0`) configured for consistent deployment.
- **Legacy Patching:** Includes a custom fix for **PyTorch 2.6+** to handle legacy YOLOv5 weight loading (`weights_only=False` security bypass).
- **Automated MLOps Pipeline:** Handles automated directory cleanup and result routing within the Docker virtual filesystem.

## 🛠️ Tech Stack
- **Backend:** Flask (Python)
- **Models:** YOLOv8 (Ultralytics) & YOLOv5 (Legacy Script)
- **Infrastructure:** Docker
- **Frontend:** HTML5, CSS3, Bootstrap 4

## 📁 Project Structure
```text
.
├── app.py              # Flask server & Threading logic
├── Dockerfile          # Multi-layer Docker configuration
├── requirements.txt    # ML and Web dependencies
├── static/
│   ├── best.pt         # YOLOv8 Weights
│   └── yolov5/         # YOLOv5 Source & Weights
├── templates/          # UI Components
└── .dockerignore       # Build optimization
```
🚀 Quick Start
1. Build the Image
```docker build -t yolo-flask-app . ```
2. Run the Container
```docker run -p 5000:5000 yolo-flask-app```
3. Usage
Navigate to http://localhost:5000, upload an image of a parking lot, and view the comparative results from both models.
