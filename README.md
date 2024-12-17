# Autonomous Vehicle Control System with Computer Vision and Neural Networks

This project involves an autonomous vehicle control system using computer vision and neural networks to predict steering and throttle commands based on camera input. The system includes modules for data collection, model training, and real-time prediction.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
  - [1. Data Collection](#1-data-collection)
  - [2. Model Training](#2-model-training)
  - [3. Real-Time Prediction](#3-real-time-prediction)


## Features

- **Data Collection**: Collects training data using a joystick and camera for capturing images with steering and throttle labels.
- **Model Training**: Trains a convolutional neural network (CNN) to predict steering and throttle from images.
- **Real-Time Prediction**: Deploys the trained model for real-time vehicle control based on camera input.
- **GPIO Motor and Servo Control**: Uses GPIO pins to control motor and steering servo for autonomous driving.

## Requirements

- Python 3.x
- OpenCV (wcv2w)
- PyTorch
- gpiozero
- pygame
- matplotlib
- pandas
- numpy

## Installation

1. **Clone the Repository:**

   ``` bash
   git clone https://github.com/HarrisonBounds/FlashFire.git
   cd autonomous-vehicle-control
   ```

2. **Set Up a Virtual Environment (Optional):**

   ``` bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
   
4. **Install Dependencies:**

   ``` bash
   pip install -r requirements.txt
   ```

   *If `requirements.txt` is not provided, install manually:*

   ``` bash
   pip install opencv-python torch torchvision gpiozero pygame matplotlib pandas numpy
   ```

## Usage

### 1. Data Collection

Collect data using a joystick to control the vehicle while capturing images and recording steering and throttle inputs.

**Steps:**

1. **Connect a Joystick** and **Set Up the Camera**.
2. **Run the Data Collection Script:**

   ``` bash
   python data_collection.py
   ```

3. **Navigate** the vehicle while the script captures images and records inputs in the `data/` directory.

### 2. Model Training

Use the collected data to train a CNN model for predicting steering and throttle commands.

**Steps:**

1. **Specify Dataset Path**: Pass the dataset directory as a command-line argument.

2. **Run the Training Script:**

   ``` bash
   python train.py data/2023_12_01_15_30  # Replace with your dataset path
   ```

3. **Training Process**: The script will train the model and save it along with training graphs and loss metrics.

### 3. Real-Time Prediction

Deploy the trained model for real-time prediction and vehicle control.

**Steps:**

1. **Specify Model Path**: Pass the trained model path as a command-line argument.

2. **Run the Autopilot Script:**

   ``` bash
   python autopilot.py models/your_model.pth
   ```

3. **Observe**: The vehicle will use the camera feed to control steering and throttle autonomously.


### Credits
Harrison Bounds - hbounds1@cub.uca.edu
Brandon Donaldson - bdonaldson1@cub.uca.edu
Lawan Hamidou - ldjibrilhamidou@cub.uca.edu

