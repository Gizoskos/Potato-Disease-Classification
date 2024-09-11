! All codes are in training file.


# Potato Disease Classification

This project aims to classify potato leaf diseases using Convolutional Neural Networks (CNNs) and TensorFlow, offering an end-to-end solution that includes data preprocessing, model building, and deployment. The classification can be performed on mobile devices through a React Native app, utilizing TensorFlow Lite and Google Cloud for backend functions.

## Project Overview

The process for the potato disease classification is illustrated in the flow diagram below (refer to the first image for details):

1. **Data Collection & Preprocessing**: 
   - Images of potato leaves are collected, cleaned, and preprocessed.
   - Data augmentation techniques are applied to expand the dataset and improve model robustness.
   
2. **Model Building**: 
   - A Convolutional Neural Network (CNN) is trained on the preprocessed dataset.
   - TensorFlow is used to build and train the model.
   
3. **Model Optimization & Conversion**: 
   - After training, the model is optimized using quantization and converted to TensorFlow Lite for deployment on mobile devices.
   
4. **Mobile & Backend Integration**: 
   - The model is integrated into a React Native application for real-time disease detection.
   - Google Cloud Functions handle backend operations, such as model serving and processing requests.

## Technologies Used

The technologies and tools required for this project are highlighted in the second image:

- **TensorFlow**: For building and training the CNN model.
- **TensorFlow Lite**: For deploying the model to mobile devices.
- **React Native**: To build the mobile application for disease detection.
- **Google Cloud Platform (GCP)**: For backend services, including hosting the model and handling API requests.
- **FastAPI**: Used for serving the trained model in the backend.
- **GCP Functions**: For processing incoming requests from the mobile app.
- **CNN (Convolutional Neural Networks)**: A deep learning algorithm used for image classification.
- **Data Augmentation**: Techniques used to enhance the dataset by applying transformations like rotation, flipping, and zooming.

### Prerequisites

Before you begin, ensure you have met the following requirements:

- A machine with Python 3.7+ installed.
- TensorFlow and related libraries installed (see the Installation section below).
- Basic understanding of Python, machine learning, and deep learning concepts.
  
## Installation Guide

### 1. Clone the Repository
First, clone this repository to your local machine:
```bash
git clone https://github.com/Gizoskos/Potato-Disease-Classification.git
```

### 2. Install TensorFlow and Required Libraries
Install TensorFlow and the necessary libraries using `pip`:
```bash
pip install tensorflow numpy matplotlib fastapi uvicorn pillow
```

### 3. TensorFlow Lite Installation
You need TensorFlow Lite to convert the trained model for mobile use:
```bash
pip install tflite-support
```

### 4. Setting Up React Native
Follow these steps to set up React Native for mobile app development:
- [React Native CLI Installation Guide](https://reactnative.dev/docs/environment-setup)

### 5. Google Cloud Functions & GCP Setup
For deploying the model to GCP and handling backend services:
- [Setting Up GCP Functions](https://cloud.google.com/functions/docs/quickstart)
- [Deploying TensorFlow Models on GCP](https://cloud.google.com/tpu/docs/tensorflow-quickstart)

## Usage

1. **Data Preprocessing**: Start by preparing the dataset. The `Data Cleaning & Preprocessing` stage involves loading the images, applying augmentation, and preparing them for model training.

2. **Model Training**: Use the CNN architecture provided in the repository to train the model on the potato disease dataset.

3. **Model Conversion**: Once the model is trained, it is converted to TensorFlow Lite format using the following code:
```python
converter = tf.lite.TFLiteConverter.from_saved_model('path_to_saved_model')
tflite_model = converter.convert()
```

4. **Mobile Deployment**: The model is deployed in a React Native app for real-time disease classification. The mobile app takes a picture of a potato leaf, sends the image to the backend, and returns the disease classification result.

## How It Works

1. **Image Input**: The user takes a picture of a potato leaf using the mobile app.
2. **Backend Processing**: The image is sent to the backend hosted on Google Cloud, which processes the image using the trained CNN model.
3. **Prediction Result**: The mobile app displays the disease classification result, helping farmers and agricultural experts diagnose potato leaf diseases.

## Contribution

Feel free to open issues or contribute by submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

