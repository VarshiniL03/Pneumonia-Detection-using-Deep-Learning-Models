# Pneumonia-Detection-using-Deep-Learning-Models
Developed a web-based diagnostic tool using CNN models for early pneumonia detection from chest X-rays.

📂 Dataset

* Source: [Kaggle - Pediatric Pneumonia Chest X-ray](https://www.kaggle.com/datasets/andrewmvd/pediatric-pneumonia-chest-xray)

🧠 Model Pipeline Overview

1. Data Loading & Preprocessing
   * Dataset is split into training, validation, and testing sets.
   * Images are resized to `(128, 128)` and normalized.
   * Extensive **data augmentation** is applied using `ImageDataGenerator`.

2. Model Architecture
   * The project uses **Transfer Learning** with a pre-trained **VGG19** model from Keras Applications.
   * The base model is followed by layers like `GlobalAveragePooling2D`, `Dense`, and `Dropout` for binary classification.
        
     System Architecture
  
       ![image](https://github.com/user-attachments/assets/e868ea0d-3359-49b5-b79e-20ff9e498cbb)

3. Training & Evaluation
   * Loss function: `binary_crossentropy`
   * Optimizer: `Adam`
   * Performance metrics: **Accuracy**, **Precision**, **Recall**, **F1-score**
   * Uses callbacks like `ModelCheckpoint` and `ReduceLROnPlateau`
   * Visualizes training curves to assess model performance.

4. Deployment-Ready Output
   * Final trained model is saved for future inference.
   * Test-time predictions are performed on sample X-ray images.
  
       Patients Dashboard
     
         ![image](https://github.com/user-attachments/assets/85d655ba-821a-4150-abf4-28180c0a5485)

       Results Page
     
         ![image](https://github.com/user-attachments/assets/d32df341-e55c-4ee6-94f2-4b979e641d95)

📊 Tools & Libraries Used
* `TensorFlow` / `Keras`
* `NumPy`, `Matplotlib`, `Seaborn`
* `scikit-learn` for metrics and validation
* `imbalanced-learn (SMOTE)` for class balancing
* `Kaggle API` for dataset access

📦 Requirements
* tensorflow>=2.9.0
* keras>=2.9.0
* numpy
* matplotlib
* seaborn
* scikit-learn
* imbalanced-learn
* kaggle
