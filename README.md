# Speaker Verification System

## Overview

This project implements a Speaker Verification System, where the goal is to determine whether a given audio sample belongs to a specific target speaker or not. The model classifies input audio as either:
Target Speaker (1) 
Non-Target Speaker (0)
The system utilizes deep learning techniques and spectrogram analysis to distinguish between different speakers based on their unique voice characteristics.

## Dataset
The dataset was collected from Kaggle, which contains recordings of 50 different speakers. To create the dataset for this project:
A target speaker (speaker number 26) was chosen from the available 50 speakers.
The non-target class was created by sampling audios from other speakers in the dataset.
The dataset was augmented using various audio transformations to increase the data for target class.

### Target audio folder : https://drive.google.com/drive/folders/1jBD6RE-lE7GsF3TgafoW8Xkb8NDU5tj0?usp=sharing

### Non target audio folder: https://drive.google.com/drive/folders/168ZO_Etu3yhFv227u4Y9FOkGtcj0k0Qu?usp=sharing

## Approach
The approach used for this speaker verification system involves several key steps:

### Data Preprocessing:
Audio samples are resampled to a standard sampling rate.
Mel Spectrograms are extracted from each audio sample to serve as input features for the model.

### Data Augmentation:
Since the dataset contained a limited number of target speaker samples, augmentation techniques were applied, including:
Pitch Shifting (Altering frequency)
Adding Noise (Background noise simulation)
Volume Modification (Increasing or decreasing amplitude)
Time Shifting (Sliding waveform forward or backward)

## Model Architecture:
A Convolutional Neural Network (CNN) is used to classify speakers based on their spectrogram representations.
The CNN model extracts spatial features from spectrograms to identify voice patterns.
A Binary Classification Head is used to determine whether the input audio belongs to the target speaker or not.

## Evaluation:
The model is tested on unseen audio samples to check its classification accuracy.
Performance metrics such as accuracy, precision, recall, and F1-score are computed to assess effectiveness.
### Accuracy: 0.9860
### Precision: 0.9844
### Recall: 1.0000
### F1-Score: 0.9921
