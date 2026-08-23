# CIFAR-10 Image Classification Using CNNs

A computer vision project that implements and compares a Traditional Convolutional Neural Network (CNN) with a Customized CNN for multi-class image classification on the CIFAR-10 dataset.

## Overview

The project explores how different CNN architectures perform on image classification tasks. A Traditional CNN is developed as a baseline and compared with a Customized CNN designed with additional architectural and regularization techniques.

The models are evaluated using test accuracy and their classification performance is analyzed to understand the effectiveness of the customized architecture.

## Objective

* Implement a Traditional CNN for image classification.
* Develop a Customized CNN architecture.
* Train both models on the CIFAR-10 dataset.
* Compare their performance using test accuracy.
* Analyze the improvement achieved by the Customized CNN.

## Dataset

The project uses the **CIFAR-10** dataset.

* **Total images:** 60,000
* **Image type:** RGB
* **Image size:** 32 × 32 pixels
* **Number of classes:** 10
* **Training images:** 50,000
* **Test images:** 10,000

### CIFAR-10 Classes

* Airplane
* Automobile
* Bird
* Cat
* Deer
* Dog
* Frog
* Horse
* Ship
* Truck

## Models

### 1. Traditional CNN

The Traditional CNN is implemented as a baseline model for comparison. It uses convolutional layers, pooling, fully connected layers, and dropout for image classification.

### 2. Customized CNN

The Customized CNN introduces architectural improvements and regularization techniques to improve generalization and classification performance.

The customized approach includes techniques such as:

* Additional convolutional layers
* Batch Normalization
* Dropout
* Data Augmentation
* Additional dense layers

## Results

| Model           | Test Accuracy |
| --------------- | ------------: |
| Traditional CNN |    **73.85%** |
| Customized CNN  |    **76.28%** |

The Customized CNN achieved a **2.43 percentage-point improvement** in test accuracy compared with the Traditional CNN.

## Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Google Colab**

## Project Structure

```text
cifar10-cnn-image-classification/
│
├── Traditional_and_Customized_CNN_CIFAR10.ipynb
├── traditional_cnn_model.keras
├── custom_cnn_model.keras
└── README.md
```

## Key Learning Outcomes

Through this project, I explored:

* Convolutional Neural Networks for image classification
* CNN architecture design
* Data augmentation
* Batch normalization
* Dropout and regularization
* Model evaluation
* Confusion matrix and classification analysis
* Comparison of baseline and customized deep learning models

## Conclusion

The Customized CNN achieved better test accuracy than the Traditional CNN, demonstrating the benefit of architectural improvements and regularization techniques for CIFAR-10 image classification.

This project provided practical experience in designing, training, evaluating, and comparing deep learning models for computer vision.

## Author

**Milan Choudhary**

Computer Science & Engineering (Artificial Intelligence)
