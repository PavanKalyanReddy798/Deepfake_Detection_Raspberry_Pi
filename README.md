Project Title

Raspberry Pi-Enabled Multi-Modal AI System for Deepfake Detection in Multimedia

Overview

This project presents a real-time deepfake detection system capable of analyzing images, videos, and audio using lightweight deep learning models deployed on a Raspberry Pi edge device.

The system performs local inference using TensorFlow Lite, enabling fast, low-latency detection without relying on cloud computing. It integrates hardware components such as an LCD display and buzzer to provide immediate visual and audio alerts when manipulated media is detected.

Problem Statement

Deepfake technology enables the creation of highly realistic manipulated multimedia content that is difficult to detect manually. Existing detection systems have several limitations:

Focus on a single media type (image or video only)
Require high computational resources
Depend on cloud-based processing
Introduce latency and privacy concerns

This project addresses these issues by developing a portable, low-cost, multi-modal deepfake detection system using edge computing.

Objectives
Detect deepfake images, videos, and audio
Implement real-time detection on Raspberry Pi
Use lightweight deep learning models
Provide output through LCD display and buzzer alert
Develop a cost-effective embedded AI system
Key Features
Multi-modal detection (image, video, audio)
Edge-based processing (no cloud dependency)
Real-time inference using TensorFlow Lite
LCD display for result visualization
Buzzer alert for fake detection
Portable and low-power system
System Architecture

Input (Image / Video / Audio)
↓
Preprocessing (Resize, Frame Extraction, Spectrogram)
↓
Deep Learning Models

MobileNetV2 (Image and Video)
LCNN (Audio)
↓
TensorFlow Lite Inference
↓
Raspberry Pi Processing
↓
Output (Monitor + LCD Display + Buzzer Alert)
Methodology
1. Input Module

The system accepts multimedia input in the form of images, videos, audio files, or real-time webcam data.

2. Preprocessing
Images are resized to 224x224 and normalized
Videos are split into frames and resized
Audio signals are converted into Mel spectrograms
3. Feature Extraction
CNN extracts spatial features from images and video frames
Spectrogram features are used for audio analysis
4. Model Processing
MobileNetV2 is used for image and video detection
LCNN is used for audio deepfake detection
5. Deployment
Models are converted to TensorFlow Lite format
Deployed on Raspberry Pi for efficient edge inference
6. Output
Results displayed on monitor and LCD
Buzzer activated when fake content is detected
Hardware Components
Raspberry Pi 4 Model B
USB Webcam
16x2 LCD Display (I2C)
Buzzer Module
Memory Card
Power Supply
Software Requirements
Python
OpenCV
TensorFlow Lite
NumPy
Librosa
Raspberry Pi OS
Project Structure

deepfake-detection-raspberry-pi/
│
├── src/
│ ├── image_check.py
│ ├── video_check.py
│ ├── audio_check.py
│ ├── lcd.py
│ └── threshold.py
│
├── models/
│ ├── image_model.tflite
│ ├── video_model.tflite
│ └── audio_model.tflite
│
├── docs/
│ ├── report.pdf
│ └── presentation.pptx
│
├── hardware/
│ └── wiring_diagram.png
│
├── outputs/
│ └── results/
│
├── README.md
├── requirements.txt

Installation

Clone the repository:
git clone https://github.com/PavanKalyanReddy798/deepfake-detection-raspberry-pi.git

Navigate to project directory:
cd deepfake-detection-raspberry-pi

Install dependencies:
pip install -r requirements.txt

Usage

Run image detection:
python src/image_check.py

Run video detection:
python src/video_check.py

Run audio detection:
python src/audio_check.py

Results

Accuracy: 94.2%
Precision: 93.6%
Recall: 92.8%
F1 Score: 93.2%

The system performs efficiently on Raspberry Pi with real-time output.

Limitations
Limited dataset (prototype system)
Frame-based video analysis (no temporal modeling)
Reduced performance on high-quality deepfakes
Audio detection requires further optimization
Future Scope
Real-time continuous monitoring system
Advanced models such as transformers
Web and mobile application integration
Larger dataset training
Improved accuracy and robustness
Applications
Social media verification
Cybersecurity systems
Digital forensics
Fake news detection
Identity fraud prevention
Publication

Published in International Journal of Emerging Technologies and Innovative Research (JETIR)
Volume 13, Issue 3, March 2026
ISSN: 2349-5162

Authors

P. Pavan Kalyan Reddy
P. Sravanthi
T. Baby Shalini
N. Bhavya
D. Ajay

License

This project is intended for academic and research purposes only.
