# Ethnicity-Recognition-with-Facial-Features

## Overview

This project is inspired by the research article titled "Recognizing Human Races through Machine Learning—A Multi-Network, Multi-Features Study" by Adrian Sergiu Darabant, Diana Borza, and Radu Danescu. The aim of this implementation is to replicate and extend the findings of the paper, comparing how different models perform in analyzing facial features for multi-class ethnicity recognition, highlighting the potential advantages of ResNetV2 in this specific scenario.  Additionally, we explore the impact of a custom, limited dataset size on model accuracy compared to the paper's findings.

## Article Reference

- **Title**: Recognizing Human Races through Machine Learning—A Multi-Network, Multi-Features Study
- **Authors**: Adrian Sergiu Darabant, Diana Borza, and Radu Danescu
- **Link to Article**: [Link to Article](https://www.mdpi.com/2227-7390/9/2/195)

## Models 

Model 1 : ResNet50


Model 2 : ResNet50V2


Model 3 : VGG16


## FACES-1 Dataset

This project utilizes a custom dataset, FACES-1,  comprising approximately 700 images. Each image is labeled with one of seven predefined ethnicity categories. The dataset serves as the foundation for training and evaluating the implemented deep learning models.

## Labels/Classes

0. Caucasian
1. East-Asian
2. Latin-American
3. Middle-Eastern
4. North-African
5. South-Asian
6. Sub-Saharian
   
###  Preprocessing:

-Face Detection and Cropping: The MTCNN (Multi-task Cascaded Convolutional Neural Network) algorithm is employed to detect faces within each image. Detected faces are then cropped and resized to 224x224 pixels for consistency.
-Normalization: Pixel values of each image are normalized to a range of 0 to 1 by dividing them by 255. This helps stabilize model training and convergence.

   ###  Sample of proprocesses images from the dataset
   ![Capture](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/3056885f-56f3-40a8-8097-fcf368bb24f7)
   
   ### Data Distribution
   
   ![2](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/2f76672e-3bf5-4986-a757-9ad285bf060b)
   
  ### Exploratory Data Analysis 

  ![3](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/57976f82-2ed0-40ae-a233-bbb2bc62942c)



## Comparative Analysis

The project includes a comparative analysis of the implemented models:

- **ResNet50**
  ResNet50 is a deep convolutional neural network architecture known for its residual blocks. It is widely used in image recognition tasks and has 50 layers. The architecture enables training deeper networks, mitigating the vanishing gradient problem.
  
  - ROC Curve:
    ![4](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/d6de2d60-bdfd-4db1-992a-513e9e8c36d3)

  - Classification Report:
     ![7](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/609a7469-f79b-4ec0-8e8c-9de89e0e95c0)

  - **Interpretation:**
    - **Accuracy:** 17%
    - **Observations:**
      - Most classes have very low precision, recall, and F1-score, suggesting poor model performance.

- **ResNet50V2**
  ResNet50V2 is an improved version of ResNet50, addressing some of its limitations. It introduces various optimizations, including a revised residual block design, leading to better performance and faster convergence.

  - ROC Curve:
    ![5](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/e716e8cd-3e9b-4dbf-a49f-641962279776)

  - Classification Report:
     ![8](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/a58be5d6-684b-488f-800b-b167a0dd516a)

  - **Interpretation:**
    - **Accuracy:** 58%
    - **Observations:**
      - Improved overall accuracy compared to Model 1.
        

- **VGG16**
  VGG16 is a classic convolutional neural network architecture that gained popularity due to its simplicity. It has 16 weight layers and is known for its uniform architecture, using small 3x3 convolutional filters.

  - ROC Curve:
     ![6](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/a52522d5-b971-4b6a-9074-09410ac27184)

  - Classification Report:
     ![9](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/bda3d67f-51e9-48ce-a413-3ba08e64b0a0)

  - **Interpretation:**
    - **Accuracy:** 23%
    - **Observations:**
      - The model has challenges predicting several classes, resulting in low precision, recall, and F1-scores for most classes.
     
      ###AUC Differences:

-ResNetV2: Achieved the highest AUC of 0.92.
-ResNet50: Achieved a lower AUC of 0.62.
-VGG16: Achieved a lower AUC of 0.63.
The significant difference in AUC between ResNetV2 and the other models further emphasizes its strength in this specific application.

![10](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/e93de84d-c08e-44c0-9090-cd759bc4ed9b)

### General Observations:

The project conducted a comparative analysis to assess the performance of various deep learning models for ethnicity recognition using facial features. Here's a summary of the key takeaways:

-**ResNetV2's Superiority**: ResNetV2 consistently outperformed ResNet50 and VGG16 in terms of overall accuracy ([58%]) and Area Under the ROC Curve (AUC) (0.92). This highlights its potential effectiveness for multi-class, multi-feature ethnicity recognition tasks, even with the limitations of a small dataset.
-**Limited Dataset Impact**: The relatively small size of the FACES-1 dataset likely contributed to the lower accuracies observed compared to the findings in the reference article [1]. A larger dataset might lead to improved model performance for all architectures.
-**Exploration Efforts**: While this study experimented with different model architectures, hyperparameters, and data preprocessing techniques (including face detection and normalization) to enhance overall performance, ResNetV2 consistently achieved superior results. This observation aligns with the findings of the referenced article, suggesting ResNetV2's inherent suitability for this task, even under constraints.

    ![10](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/f4c3e006-283a-4ed5-8a7c-ad8b25e829f8)

    ![11](https://github.com/najwanaamane/Ethnicity-Recognition-with-Facial-Features/assets/86806375/ba3f81e6-5d1f-4358-8750-7482680f1021)

    



