# Emotion Detection

## Description
This project implements an Emotion Detection system using a Convolutional Neural Network (CNN) to detect facial expressions in real-time through a webcam feed. The system recognizes seven basic emotions: Angry, Disgusted, Fearful, Happy, Neutral, Sad, and Surprised. It utilizes OpenCV for face detection and Keras for building and training the CNN model.

## Tools & Libraries
- Python (Version 3.x)
- OpenCV (cv2)
- Keras
- NumPy

## Dataset
The CNN model is trained on the FER2013 dataset, which consists of 35,887 grayscale images of faces labeled with seven different emotions. The dataset is preprocessed and split into training and testing sets.

## Model Training
- The CNN model architecture consists of multiple Conv2D and MaxPooling2D layers, followed by Dropout layers to prevent overfitting.
- The model is trained using the Adam optimizer and categorical cross-entropy loss function.
- The training process involves training the model on the training set for 50 epochs with a batch size of 64.
- After training, the model structure is saved in a JSON file (`emotion_model.json`), and the trained weights are saved in an HDF5 file (`emotion_model.h5`).

## Model Evaluation
- The trained model is loaded from the saved files (`emotion_model.json` and `emotion_model.h5`) for real-time emotion detection.
- The model is applied to each frame captured from the webcam feed to detect faces and predict the corresponding emotions.
- The detected emotions are overlaid on the video feed in real-time.

## Usage
To use the Emotion Detection system:
1. Ensure that the required libraries are installed (OpenCV, Keras, NumPy).
2. Run the Python script containing the code.
3. The webcam feed will start, and the system will detect faces and predict emotions in real-time.
4. Press 'q' to exit the application.
