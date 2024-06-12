# Digit Recognizer Pipeline

## Project Overview

This project aims to build a pipeline for digit recognition using the KubeFlow Pipelines (KFP) framework. The pipeline consists of several components for dataset retrieval, preprocessing, model building, training, evaluation, and storage. It is designed to be scalable and reproducible, facilitating easy experimentation and deployment of machine learning models.

## Components

1. **get_data_batch**: This component retrieves the dataset, preprocesses it, and stores it in a MinIO bucket. It splits the dataset into training and testing sets and saves them in the MinIO bucket.

2. **reshape_data**: This component reshapes the data for model building. It retrieves the preprocessed data from the MinIO bucket, reshapes it according to the model's input requirements, normalizes it, and then saves it back to the MinIO bucket.

3. **model_building**: This component builds a Convolutional Neural Network (CNN) model using Keras API for digit recognition. It compiles the model, trains it on the training data, evaluates its performance on the test data, generates a confusion matrix, saves the model to MinIO, and returns metadata and metrics.

## Pipeline Flow

1. **Data Retrieval and Preprocessing**: The `get_data_batch` component is executed first to fetch the dataset, split it into training and testing sets, and store them in the MinIO bucket.

2. **Data Reshaping**: The `reshape_data` component is executed to reshape the data into the required format for model training.

3. **Model Training and Evaluation**: The `model_building` component is executed to build, train, and evaluate the CNN model. It also generates a confusion matrix and saves the model to MinIO.

## Image Prediction

To test the model's prediction capability, an image named "img1.jpg" containing the number 3 is provided as input. When fed into the trained model, it correctly predicts the digit as 3. The prediction results are stored and can be further analyzed for model validation and improvement.

## Source:

### I base from this author and video to deploy more and suitable for my project.
### Youtube name : Technology with Flo
### [YouTube link](https://www.youtube.com/watch?v=6wWdNg0GMV4)
