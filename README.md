# Part 2: Computer Vision Problem Formulation and CNN Prototype

---

# Project Overview

This project focuses on developing a Convolutional Neural Network (CNN) model for an image classification task. The primary objective was to understand how CNNs learn visual features from image data using convolution layers, pooling operations, activation functions, and dense neural network layers.

The implementation was completed using Python along with TensorFlow/Keras, OpenCV, Matplotlib, Seaborn, and Scikit-learn.

---

# Dataset Information

The dataset consists of images grouped into four categories:

- normal
- dent
- stain
- scratch

The goal of the model is to correctly classify images into their respective defect categories based on visual surface patterns.

Dataset Source Link:

https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing

---

# Task 1: Problem Identification

The provided dataset represents an Image Classification problem within the field of Computer Vision. Each image belongs to a predefined category such as normal, dent, stain, or scratch.

Image classification is the most suitable task type because the CNN model only needs to determine the correct category of an image based on its visual characteristics. The model is not required to locate objects or perform image segmentation.

CNN models are highly effective for image classification tasks because they can automatically learn visual patterns such as textures, edges, stains, and defect-related features directly from image data.

---

# Task 2: Dataset Exploration

The dataset was analyzed to understand:

- Total number of image classes
- Number of images in each category
- Sample images from every class
- Image dimensions
- Dataset distribution

### Observation

The dataset contains four categories: normal, dent, stain, and scratch. Each class contains 120 images, indicating that the dataset is balanced across all categories.

Sample images from each class were visualized to better understand the visual differences between defect patterns and surface conditions.

---

# Task 3: Image Preprocessing

The following preprocessing operations were applied:

- Resized all images to 64 × 64 pixels
- Normalized pixel values to a range between 0 and 1
- Split the dataset into training and validation/testing datasets
- Applied image augmentation techniques including:
  - Rotation
  - Zooming
  - Horizontal flipping

### Observation

Image preprocessing helped standardize the dataset for CNN training. Data augmentation improved dataset variability and helped reduce the chances of overfitting during model training.

---

# Task 4: CNN Model Creation

A Convolutional Neural Network (CNN) model was developed using the TensorFlow/Keras Sequential API.

### CNN Architecture

- Convolution Layer
- ReLU Activation Function
- Max Pooling Layer
- Flatten Layer
- Dense Layer
- Dropout Layer
- Output Layer with Softmax Activation

### Model Details

- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Output Classes: 4

### Observation

The CNN model successfully learned important visual patterns such as scratches, stains, and dents directly from image data. Pooling layers helped reduce computational complexity, while dense layers learned higher-level feature representations.

---

# Task 5: Model Training and Evaluation

The CNN model was trained for 10 epochs and evaluated using:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Confusion Matrix
- Classification Report
- Sample Predictions

### Model Performance

- Final Testing Accuracy: Approximately 84%

### Observation

Training and validation accuracy gradually improved throughout the training process, while loss values continuously decreased. The CNN model was able to correctly classify many test images based on visual defect patterns.

The confusion matrix and classification report indicated that some image classes were predicted more accurately than others. Certain defect categories shared visually similar patterns, leading to some classification difficulties.

---

# Task 6: CNN Concept Explanation

## 1. What is Convolution?

Convolution is one of the core operations in a CNN model. In this process, small filters or kernels move across an image to identify important visual patterns such as edges, textures, scratches, stains, lines, or shapes. Instead of analyzing the entire image at once, the CNN learns small visual details step by step and combines them to understand the complete image.

For example, in this project, the CNN learns to recognize features such as scratch marks, stain regions, or dents from surface images. Different filters automatically learn different visual patterns during training.

---

## 2. Why is Pooling Used?

Pooling is used to reduce the size of feature maps generated after convolution operations. This decreases computation time and improves model efficiency. Pooling also helps the model focus on the most important visual information instead of processing every individual pixel detail.

In simple terms, pooling summarizes important image features. For example, even if the position of a scratch changes slightly within an image, pooling helps the CNN continue recognizing the defect correctly. Max Pooling is commonly used because it preserves the strongest and most important image features.

---

## 3. Why is ReLU Commonly Used in CNNs?

ReLU (Rectified Linear Unit) is commonly used in CNN models because it enables faster learning and improves training performance. ReLU converts negative values into zero while keeping positive values unchanged, which simplifies computations and improves training efficiency.

Another important advantage of ReLU is that it helps prevent the vanishing gradient problem, which can slow learning in deep neural networks. Since CNN architectures contain multiple layers, ReLU helps make training faster and more stable.

---

## 4. Why are CNNs Better than Regular Feed-Forward Networks for Image Data?

CNNs are specifically designed for image processing tasks, whereas regular feed-forward neural networks are more suitable for simple numerical datasets. Images contain spatial relationships between nearby pixels, and CNNs are capable of capturing these relationships effectively through convolution and pooling operations.

For example, in this project the CNN can recognize scratches, dents, and stains based on their visual appearance and spatial patterns. A standard feed-forward network would process each pixel independently and require a very large number of parameters, making training inefficient and difficult.

CNNs automatically learn visual features directly from image data, making them more powerful and accurate for computer vision tasks such as image classification, object detection, and facial recognition.

---

# Task 7: Business Use Case Mapping

This type of computer vision solution can be extremely useful in the manufacturing industry for automated defect detection and quality inspection.

In many industries, products must be inspected for scratches, dents, stains, or damaged surfaces before delivery. Traditionally, these inspections are performed manually, which can be slow and susceptible to human error.

A CNN-based computer vision system can automate this process by analyzing product images and identifying defects in real time.

For example, in smartphone manufacturing or automobile industries, cameras can capture product images during production, and the CNN model can automatically classify defective and non-defective products. This helps improve product quality, reduce manual effort, minimize defective product delivery, and increase operational efficiency.

---

# Technologies Used

- Python
- Google Colab
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Repository Structure

```bash
part-2-cnn-computer-vision/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
├── sample_predictions/
│   └── prediction_outputs.png
└── results/
    ├── accuracy_loss_curves.png
    └── confusion_matrix.png
```

---

# Conclusion

This project provided practical understanding of CNN architecture and computer vision fundamentals. The CNN model successfully learned visual defect patterns from images and classified them into different categories with good accuracy.

The project also demonstrated how convolution layers, pooling operations, activation functions, and dense layers work together within deep learning-based image classification systems.
