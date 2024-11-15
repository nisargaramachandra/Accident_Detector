# Accident Detector
This Accident Detector uses Deep Learning to detect road accidents through live video or CCTV footage. It aims to help reduce response times for emergency services by identifying accidents in real time.

## Table of Contents
1. [Introduction](#introduction)
2. [Technologies Used](#technologies-used)
3. [Project Structure](#project-structure)
4. [Prerequisites](#prerequisites)
5. [Getting Started](#getting-started)
6. [How It Works](#how-it-works)
7. [Future Work](#future-work)

## Introduction
Road accidents are a major global issue, and faster accident detection can save lives by reducing emergency response times. This system detects accidents from live or recorded video by analyzing frames for accident-related features using a trained Deep learning model.

## Technologies Used
- **Python** for scripting
- **Deep Learning** for model training and accident detection
- **Jupyter Notebook** for training the model
- **OpenCV** for handling video and frame processing

## Project Structure
- **data/**: Contains the dataset (from Kaggle) for accident detection.
- **accident-classification.ipynb**: Jupyter notebook that trains the accident detection model and generates two important files:
  - **model.json**: Stores the model’s architecture.
  - **model_weights.h5**: Holds the weights learned during training.
- **detection.py**: Loads the model and applies it to detect accidents in live or recorded video.
- **camera.py**: Manages the camera input and runs `detection.py` on each frame to analyze and display accident predictions.

## Prerequisites
- **Python version** > 3.6
- **Python Libraries**: Install dependencies using the command below:
  ```bash
  pip install -r requirements.txt
  ```
- Basic knowledge of Python, Machine Learning, and Deep Learning is recommended for contributions.

## Getting Started
1. **Clone the repository**:
   ```bash
   git clone https://github.com/nisargaramachandra/Accident_Detector.git
   ```
2. **Install Required Packages**:
   ```bash
   pip install -r requirements.txt
   ```
   > Note: A camera is required for live detection. Alternatively, you can use a pre-recorded video file.

3. **Train the Model**:
   - Open and run `accident-classification.ipynb` to train the accident detection model. This will generate two key files: `model.json` and `model_weights.h5`.

4. **Run the System**:
   - Once the model files are ready, execute the main program:
   ```bash
   python detection.py
   ```

## How It Works
1. **Model Training**: `accident-classification.ipynb` trains a Deep Learning model to recognize accidents from labeled data. The trained model architecture and weights are saved in `model.json` and `model_weights.h5`.
2. **Detection**: `detection.py` loads the model and processes live or recorded video frames, classifying each frame as an "accident" or "non-accident" frame, with a likelihood percentage.
3. **Display**: For each frame, the system displays the likelihood of an accident, providing a real-time detection system.

## Future Work
- **Automated Alert System**: Integrate an alarm or notification system to alert nearby emergency services with accident location and severity.
- **Enhanced Severity Detection**: Develop additional model capabilities to assess accident severity, aiding emergency response prioritization.

## About
This system is designed to address road safety concerns by detecting accidents quickly through Deep Learning. It is a step towards automated and intelligent surveillance for enhanced public safety.
