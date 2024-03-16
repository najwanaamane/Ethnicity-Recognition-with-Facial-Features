# Ethnicity-Recognition-with-Facial-Features

## Overview

This project is inspired by the research article titled "Recognizing Human Races through Machine Learning—A Multi-Network, Multi-Features Study" by Adrian Sergiu Darabant, Diana Borza, and Radu Danescu. The aim of this implementation is to replicate and extend the findings of the paper, comparing how different models perform in analyzing facial features for multi-class ethnicity recognition, highlighting the potential advantages of ResNetV2 in this specific scenario.  Additionally, we explore the impact of a custom, limited dataset size on model accuracy compared to the paper's findings.

## Article Reference

- **Title**: Recognizing Human Races through Machine Learning—A Multi-Network, Multi-Features Study
- **Authors**: Adrian Sergiu Darabant, Diana Borza, and Radu Danescu
- **Link to Article**: [Link to Article](https://www.mdpi.com/2227-7390/9/2/195)

## Models

### ResNet50

ResNet50 is a deep convolutional neural network architecture known for its residual blocks. It is widely used in image recognition tasks and has 50 layers. The architecture enables training deeper networks, mitigating the vanishing gradient problem.

### ResNet50V2

ResNet50V2 is an improved version of ResNet50, addressing some of its limitations. It introduces various optimizations, including a revised residual block design, leading to better performance and faster convergence.

### VGG16

VGG16 is a classic convolutional neural network architecture that gained popularity due to its simplicity. It has 16 weight layers and is known for its uniform architecture, using small 3x3 convolutional filters.

## FACES-1 Dataset

This project utilizes a custom dataset, FACES-1,  comprising approximately 700 images. Each image is labeled with one of seven predefined ethnicity categories. The dataset serves as the foundation for training and evaluating the implemented deep learning models.

## Labels/Classes

1. Caucasian
2. East-Asian
3. Latin-American
4. Middle-Eastern
5. North-African
6. South-Asian
7. Sub-Saharian

   ![Capture](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/3056885f-56f3-40a8-8097-fcf368bb24f7)
   ![2](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/2f76672e-3bf5-4986-a757-9ad285bf060b)

  ![3](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/57976f82-2ed0-40ae-a233-bbb2bc62942c)



## Comparative Analysis

The project includes a comparative analysis of the implemented models:

- **ResNet50**
  - ROC Curve: ![4](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/d6de2d60-bdfd-4db1-992a-513e9e8c36d3)

  - Classification Report: ![7](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/609a7469-f79b-4ec0-8e8c-9de89e0e95c0)

  - **Interpretation:**
    - **Accuracy:** 17%
    - **Observations:**
      - The model struggles to predict any class accurately, resulting in an overall low accuracy.
      - Class 2 has the highest recall (90%), but precision is low (19%), indicating that when the model predicts this class, it's often incorrect.
      - Most classes have very low precision, recall, and F1-score, suggesting poor model performance.

- **ResNet50V2**
  - ROC Curve: ![5](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/e716e8cd-3e9b-4dbf-a49f-641962279776)

  - Classification Report: ![8](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/a58be5d6-684b-488f-800b-b167a0dd516a)

  - **Interpretation:**
    - **Accuracy:** 58%
    - **Observations:**
      - Improved overall accuracy compared to Model 1.
      - Class 3 has the highest recall (76%), while Class 6 has the highest precision (73%).
      - Some classes, like Class 4, have lower precision, recall, and F1-score, indicating challenges in predicting these classes accurately.

- **VGG16**
  - ROC Curve: ![6](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/a52522d5-b971-4b6a-9074-09410ac27184)

  - Classification Report: ![9](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/bda3d67f-51e9-48ce-a413-3ba08e64b0a0)

  - **Interpretation:**
    - **Accuracy:** 23%
    - **Observations:**
      - Class 4 has the highest recall (90%), but precision is low (19%), similar to Model 1.
      - The model has challenges predicting several classes, resulting in low precision, recall, and F1-scores for most classes.

### General Observations:

- **Class Imbalance:**
  - The models might be influenced by class imbalance, particularly visible in classes with low support (number of samples).
  - Techniques to handle class imbalance, such as oversampling or adjusting class weights, could be explored.
    ![10](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/f4c3e006-283a-4ed5-8a7c-ad8b25e829f8)

    ![11](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/ba3f81e6-5d1f-4358-8750-7482680f1021)

    
![12](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/83d7509b-abf5-43f9-80ef-ac7b30ab7912)



- **Recommendations:**
  - Consider exploring additional metrics and visualizations to gain a more comprehensive understanding of model performance.
  - Address class imbalance to improve model predictions for minority classes.
  - Experiment with different model architectures, hyperparameters, or data preprocessing techniques to enhance overall performance.


