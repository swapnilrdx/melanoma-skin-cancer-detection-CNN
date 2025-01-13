# Skin Cancer Classification Project

## Abstract

This project focuses on developing a Convolutional Neural Network (CNN) model to classify skin cancer images into different categories.  The model is trained and evaluated on the ISIC (International Skin Imaging Collaboration) dataset.  The project addresses class imbalance in the dataset using data augmentation techniques and explores various CNN architectures to optimize classification accuracy.

## Problem Statement

Skin cancer is a significant health concern, and early and accurate diagnosis is crucial for successful treatment.  Manually classifying skin lesions can be subjective and time-consuming.  This project aims to build a reliable automated system for skin cancer image classification, improving diagnostic efficiency and potentially aiding medical professionals.

## Model Architecture

Multiple CNN models were explored during the project, starting with a basic CNN architecture and progressing to more complex models. Key architectural components included:

* **Convolutional Layers:**  Extracted features from input images.  Different numbers of layers and filter sizes were experimented with.
* **MaxPooling Layers:**  Reduced dimensionality and computational complexity while retaining important features.
* **Batch Normalization:**  Stabilized training, improved performance, and reduced training time.
* **Dropout Layers:**  Prevented overfitting by randomly deactivating neurons during training.
* **Dense (Fully Connected) Layers:**  Combined extracted features to perform classification.
* **Softmax Activation:**  Produced probabilities for each class in the final layer.


Two main models were compared:
1. **CNN_6_Conv2D + 3_BN_local.keras**: This model features 6 convolutional layers, 3 batch normalization layers, and achieved good performance, balancing accuracy and computational efficiency.
2. **CNN_6_Con2D + 3 BN + 3_Drop_local.keras**:  This model utilizes additional dropout layers to explicitly address overfitting, providing another perspective on model regularization.

## Technologies Used

* **Python:**  Primary programming language for data preprocessing, model development, and evaluation.
* **TensorFlow/Keras:**  Deep learning framework for model building, training, and deployment.
* **NumPy:**  For numerical operations and array manipulation.
* **Pandas:**  For data analysis and manipulation.
* **Matplotlib & Seaborn:**  For data visualization.
* **Augmentor:**  For data augmentation to address class imbalance.
* **PIL (Pillow):**  For image processing.
* **Scikit-learn (potential):** While not explicitly shown in the provided code, it's likely used for certain evaluation metrics.


## Data Augmentation

The original dataset exhibited class imbalance. The Augmentor library was used to generate additional images for the less represented classes, enhancing the model's ability to learn patterns from these classes and improving overall performance.


## Model Training and Evaluation

The models were trained with the Adam optimizer and the Sparse Categorical Crossentropy loss function.  The performance was monitored using accuracy and validation accuracy. ModelCheckpoint and EarlyStopping callbacks were used to save the best model and prevent overfitting. The trained models were then evaluated on the test set.


## Results and Analysis

Detailed analysis of the models' performance, including training and validation accuracy and loss plots, can be found within the code comments. Performance varied depending on the model architecture.  The impact of data augmentation and model complexity on model performance was observed and discussed.


## Future Work

* **Hyperparameter Tuning:** Further optimization of hyperparameters like learning rate, batch size, and optimizer settings to enhance performance.
* **Model Ensembling:** Combining predictions from multiple models to potentially improve accuracy.
* **More Advanced Architectures:** Exploring more sophisticated architectures like EfficientNet or ResNet.
* **Cross-Validation:**  Robust performance evaluation using cross-validation.
