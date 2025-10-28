# CNN Age and Gender Recognition

This repository contains a Multi-Output Convolutional Neural Network (CNN) model built with TensorFlow/Keras for simultaneous Age Regression and Gender Classification from facial images.

The model uses a shared convolutional backbone with two separate, specialized prediction heads—one for age and one for gender—trained on the large-scale UTKFace dataset.

Features:
  Multi-Task Learning: A single CNN architecture efficiently predicts two distinct attributes (age and gender).
  Data Pipelining: Uses tf.data.Dataset for efficient data loading, preprocessing, and augmentation.
  UTKFace Integration: Includes logic to parse age and gender directly from the UTKFace image filenames.
  Keras Callbacks: Implements ModelCheckpoint and EarlyStopping for robust training.

