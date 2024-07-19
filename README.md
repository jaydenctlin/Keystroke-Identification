# Keystroke Identification using Deep Learning

This repository contains the implementation of different deep learning architectures for the task of identifying keystrokes from recording audio files. Specifically, this project explores the use of Basic Convolutional Neural Networks (CNN) and Denoising Autoencoder with Classifier.

## Overview

The goal of this project is to identify keystrokes from audio recordings by transforming the audio files into Mel Spectrogram images and applying deep learning models to classify the keystrokes. This work builds upon an original study that tested the CoAtNet architecture, and extends it by evaluating the performance of Basic CNN and Denoising Autoencoder with Classifier.

This is a course project for ST456 Deep Learning.

## Data Augmentation

Data augmentation is a crucial technique used to enrich the training dataset by generating additional observations through various transformations applied to the original samples. In this study, we employ the following alteration processes: addition of Gaussian noise, time masking, frequency masking, and time shifts. These techniques are especially important to improve the real-life applicability of the models by simulating real-world variability and enhancing the model’s robustness.

## Models Implemented

### 1. Basic CNN

The Basic Convolutional Neural Network (CNN) is a straightforward approach that applies multiple convolutional layers followed by pooling layers to extract features from the Mel Spectrogram images. The extracted features are then passed through fully connected layers to perform classification.

#### Key Features:
- Multiple convolutional layers for feature extraction
- Pooling layers to reduce dimensionality
- Fully connected layers for classification
- Achieved 85% test accuracy

### 2. Denoising Autoencoder with Classifier

The Denoising Autoencoder with Classifier is a two-stage model. The first stage is an autoencoder that learns to reconstruct the input Mel Spectrogram images while denoising them. The second stage uses the encoded features from the autoencoder as input to a classifier for keystroke identification.

#### Key Features:
- Denoising autoencoder for feature learning and noise reduction
- Separate classifier stage for final classification
- Achieved 93% test accuracy

## Results

Both the Basic CNN and Denoising Autoencoder with Classifier showed promising results. The Basic CNN achieved an 85% test accuracy, while the Denoising Autoencoder with Classifier achieved a 93% test accuracy.

## Repository Structure

- `Code/`: Contains the implementations of the Basic CNN and Denoising Autoencoder with Classifier, as well as the script for importing audio data.
- `Raw_data/`: Contains audio files.
- `KeystrokeAnalysis.pdf`: Comprehensive analysis report.
