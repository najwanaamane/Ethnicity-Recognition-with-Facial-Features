# Ethnicity-Recognition-with-Facial-Features

## Overview

This project is inspired by the research article titled "Recognizing Human Races through Machine Learning—A Multi-Network, Multi-Features Study" by Adrian Sergiu Darabant, Diana Borza, and Radu Danescu. The aim of this implementation is to replicate and extend the findings of the paper, exploring ethnicity recognition using deep learning models and multiple features.

## Article Reference

- **Title**: Recognizing Human Races through Machine Learning—A Multi-Network, Multi-Features Study
- **Authors**: Adrian Sergiu Darabant, Diana Borza, and Radu Danescu
- **Link to Article**: [Link to Article](provide_link_here)

## Models

### ResNet50

ResNet50 is a deep convolutional neural network architecture known for its residual blocks. It is widely used in image recognition tasks and has 50 layers. The architecture enables training deeper networks, mitigating the vanishing gradient problem.

### ResNet50V2

ResNet50V2 is an improved version of ResNet50, addressing some of its limitations. It introduces various optimizations, including a revised residual block design, leading to better performance and faster convergence.

### VGG16

VGG16 is a classic convolutional neural network architecture that gained popularity due to its simplicity. It has 16 weight layers and is known for its uniform architecture, using small 3x3 convolutional filters.

## FACES-1 Dataset

The FACES-1 dataset comprises approximately 700 images, with each image belonging to one of the seven predefined ethnicity labels. The dataset is designed for facial feature-based ethnicity recognition and serves as the basis for training and evaluating the deep learning models in this project.

## Labels/Classes

1. Caucasian
2. East-Asian
3. Latin-American
4. Middle-Eastern
5. North-African
6. South-Asian
7. Sub-Saharan

## Comparative Analysis

The project includes a comparative analysis of the implemented models:

- **ResNet50**
  - ROC Curve: [Image Link]
  - Classification Report: [Textual Report]
  - Test Accuracy: [Accuracy Percentage]
  - **Interpretation:**
    - **Accuracy:** 17%
    - **Observations:**
      - The model struggles to predict any class accurately, resulting in an overall low accuracy.
      - Class 2 has the highest recall (90%), but precision is low (19%), indicating that when the model predicts this class, it's often incorrect.
      - Most classes have very low precision, recall, and F1-score, suggesting poor model performance.

- **ResNet50V2**
  - ROC Curve: [Image Link]
  - Classification Report: [Textual Report]
  - Test Accuracy: [Accuracy Percentage]
  - **Interpretation:**
    - **Accuracy:** 58%
    - **Observations:**
      - Improved overall accuracy compared to Model 1.
      - Class 3 has the highest recall (76%), while Class 6 has the highest precision (73%).
      - Some classes, like Class 4, have lower precision, recall, and F1-score, indicating challenges in predicting these classes accurately.

- **VGG16**
  - ROC Curve: [Image Link]
  - Classification Report: [Textual Report]
  - Test Accuracy: [Accuracy Percentage]
  - **Interpretation:**
    - **Accuracy:** 23%
    - **Observations:**
      - Class 4 has the highest recall (90%), but precision is low (19%), similar to Model 1.
      - The model has challenges predicting several classes, resulting in low precision, recall, and F1-scores for most classes.

### General Observations:

- **Class Imbalance:**
  - The models might be influenced by class imbalance, particularly visible in classes with low support (number of samples).
  - Techniques to handle class imbalance, such as oversampling or adjusting class weights, could be explored.

- **Recommendations:**
  - Consider exploring additional metrics and visualizations to gain a more comprehensive understanding of model performance.
  - Address class imbalance to improve model predictions for minority classes.
  - Experiment with different model architectures, hyperparameters, or data preprocessing techniques to enhance overall performance.

These interpretations highlight the strengths and weaknesses of each model. Depending on the specific requirements of your application, you might need to prioritize certain classes or aspects of performance. Additionally, optimizing hyperparameters, trying different model architectures, or leveraging more advanced techniques could lead to further improvements.

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/ethnicity-recognition.git
   cd ethnicity-recognition
