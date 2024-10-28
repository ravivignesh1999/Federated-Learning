Real-Time Emotion Recognition by Facial Sentimental Analysis Using On-Device Machine Learning
This project implements an emotion recognition system that analyzes facial expressions in real-time using a hybrid Convolutional Neural Network (CNN) model optimized for on-device machine learning. It aims to offer privacy-preserving sentiment analysis by leveraging federated learning, allowing model training on user devices without the need for centralized data storage.

Table of Contents
Introduction
Features
Technologies Used
Datasets
Architecture
Installation
Usage
Results
Future Work
Contributors
License
Introduction
Emotion recognition is increasingly vital in fields like e-learning and user experience enhancement. This project uses a CNN-based model with federated learning to recognize seven emotions—neutral, anger, fear, sadness, happiness, surprise, and disgust—while keeping user data private. The model runs directly on the device, reducing latency and maintaining user privacy.

Features
Real-Time Emotion Recognition: Detects and classifies facial expressions in real-time using device cameras.
Federated Learning: Allows on-device training and updates the global model without exposing user data.
Geometric Feature Extraction: Utilizes 68 facial landmarks to improve emotion classification accuracy.
Low Model Size: Optimized model that is 80% smaller than conventional CNNs, making it suitable for mobile devices.
Privacy-Preserving: All training and inference are done locally on the device, ensuring user data privacy.
Technologies Used
TensorFlow.js: For running the model in web browsers.
Keras: Model development framework.
React Native: Interface for mobile implementation.
Dlib: For facial landmark detection and geometric feature extraction.
Datasets
KDEF (Karolinska Directed Emotional Faces): Contains 4900 images from 70 individuals showing various emotions.
JAFFE (Japanese Female Facial Expression): Consists of 213 grayscale images with seven facial expressions, used for federated simulation.
Architecture
The system combines two main components:

Hybrid CNN-MLP Architecture: A lightweight CNN model is combined with an MLP that focuses on geometric features. This design reduces model size while maintaining accuracy.
Federated Learning Environment: A client-server simulation where local model weights are aggregated into a global model without transferring raw data.
Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/your-username/real-time-emotion-recognition.git
cd real-time-emotion-recognition
Install Dependencies:

For Python environment:
bash
Copy code
pip install -r requirements.txt
For JavaScript (if using TensorFlow.js and React Native):
bash
Copy code
npm install
Set Up Datasets:

Download the KDEF and JAFFE datasets and place them in the data/ folder.
Usage
Run the Model Locally:

bash
Copy code
python main.py
Federated Simulation:

Use the federated_simulation.py script to simulate federated learning across devices.
Web Interface:

For the web interface, use TensorFlow.js and load model.json to initialize the model in the browser.
Results
The hybrid model achieves a balance between efficiency and accuracy:

Accuracy: ~67% on real-world test data, with a model size reduction of 80%.
Latency: Processes each frame in ~270 ms, enabling near-real-time inference.
Performance Metrics
Dataset	Pre-Federation Accuracy	Post-Federation Accuracy
KDEF	89.29%	82.87%
JAFFE	52.04%	74.50%
Future Work
Improved Model Tuning: Explore combining geometric features with Local Binary Patterns (LBP) to improve accuracy further.
Enhanced Federated Learning: Implement a custom aggregation algorithm to enhance the privacy and efficiency of the global model.
