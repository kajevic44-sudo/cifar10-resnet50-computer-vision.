# cifar10-resnet50-computer-vision.
CIFAR-10 image classification using ResNet50 transfer learning in TensorFlow/Keras

# CIFAR-10 Image Classification with ResNet50 Transfer Learning

This project demonstrates a complete computer vision workflow for image classification on the CIFAR-10 dataset using TensorFlow/Keras and transfer learning with ResNet50.

## Project Overview

The goal of this project is to classify CIFAR-10 images into 10 categories using a pre-trained ResNet50 model. The workflow includes dataset loading, preprocessing, exploratory data analysis, transfer learning, fine-tuning, model evaluation, confusion matrix analysis, and qualitative inspection of correct and incorrect predictions.

## Dataset

The project uses the CIFAR-10 dataset, which contains 60,000 color images of size 32x32 pixels across 10 classes. Following the project requirements, the training set was limited to 10,000 images, while the full test set of 10,000 images was used for final evaluation.

## Model Architecture

The model uses ResNet50 pre-trained on ImageNet as a convolutional feature extractor. A custom classification head was added on top of the ResNet50 base for CIFAR-10 classification.

The training process was divided into two phases:

1. Training only the custom classification head while the ResNet50 base was frozen.
2. Fine-tuning the model by unfreezing the ResNet50 base and using a lower learning rate.

## Results

The final model achieved a test accuracy of approximately **64.42%**.

Although the model achieved high training accuracy, validation and test accuracy were lower, indicating overfitting. This was expected due to the reduced training set size, the low resolution of CIFAR-10 images, and the relatively high capacity of ResNet50.

## Key Analysis Included

- Class distribution analysis
- Training and validation accuracy/loss curves
- Final test evaluation
- Confusion matrix
- Classification report
- Correct and incorrect prediction examples
- Discussion of overfitting
- Limitations and future improvements
- Optional data augmentation extension

## Technologies Used

- Python
- TensorFlow/Keras
- ResNet50
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## How to Run

## Notebook

The complete project implementation, including code, outputs, visualizations, evaluation results, and conclusions, is available in the Jupyter notebook file included in this repository.


The notebook can be opened and executed in Google Colab. Before running the notebook, enable GPU acceleration:

```text
Runtime → Change runtime type → Hardware accelerator → GPU

