# Image-Multiclass-Classification

## Project Overview
This project involves the development of a deep learning image classification system. The primary goal was to classify images into one of four distinct categories using a convolutional neural network (CNN). The project incorporates two models: a baseline VGG-like model and an improved model.

## Dataset
Each class has its own folder, containing the respective images. All images were resized to 224x224 pixels with three color channels (RGB).
I used one-hot encoding to represent the four classes, and splitted the data to 3 sets, 80% of the dataset to training set, 10% of the dataset to validation set, and the rest 10% of the dataset to test set.

## Model Architectures

### Baseline Model

Based on the VGG-16 architecture.

#### Layers:

Convolutional Layers: Five blocks, with increasing filter sizes from 64 to 512.

Pooling Layers: MaxPooling2D layers after each convolutional block.

Fully Connected Layers: Two dense layers with 4096 neurons each.

Output Layer: Dense layer with 4 neurons (softmax activation).

Activation Function: ReLU for hidden layers; Softmax for the output layer.

### Improved Model
Modifications to the baseline model:

Added Batch Normalization after each convolutional layer.

Added Dropout (rate = 0.2) in the fully connected layers to prevent overfitting.

## Evaluation Metrics
Accuracy: Overall correctness of the model.

Precision: Correctness of positive predictions, averaged across classes.

Recall: Proportion of actual positives identified correctly, averaged across classes.

F1 Score: Harmonic mean of precision and recall.

## Results

### Baseline Model

Accuracy: 24.38%

Precision: 6.09%

Recall: 25.00%

F1 Score: 9.80%

### Improved Model

Accuracy: 83.12%

Precision: 83.50%

Recall: 83.51%

F1 Score: 83.01%

## Conclusion
The improved model demonstrated a significant increase in performance compared to the baseline. Enhancements like Batch Normalization and Dropout helped address issues of overfitting and training instability, resulting in robust classification performance across all four classes.
