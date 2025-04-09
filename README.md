# AI-VAR (Football Foul Detection Using AI)
This project aims to classify football tackles into different categories (e.g., "Clean Tackles" and "Fouls") using deep learning techniques. The dataset is used to train a model that can accurately classify images of tackles in football games.

## 🗂️ Data
The [Fouls Dataset](https://www.kaggle.com/code/bshayer2000/fouls) from Kaggle is utilized, consisting of 496 images of fouls and 429 images of clean tackles.

## 🚀 Features
### 1. Data Preprocessing:
Handles image loading, augmentation, and normalization using libraries like albumentations and torchvision.

### 2. Dataset Class:

A custom dataset class (FootballTacklesDataset) for loading and transforming images.

### 3. Data Augmentation:

The project uses albumentations for data augmentation, such as:

- Horizontal flips

- Random brightness and contrast adjustments

- Random rotations and scaling

### 4. Model Setup:

- Pre-trained models such as ResNet50 and EfficientNet are used for feature extraction.

- Custom layers are added to the pre-trained models for classification tasks.

### 5. Training with Early Stopping:

- The model is trained with early stopping to prevent overfitting.

- The best model is saved based on validation loss.

### 6. Evaluation:

- Detailed evaluation with confusion matrices and classification reports.

- Plots for training and validation loss and accuracy over epochs.

### 6. GPU 
This project utilizes the Kaggle Notebook with dual T4 GPUs for accelerated training.

## 📊 Results
After training, the following results are generated:

- Loss and Accuracy: Visualize over epochs for training and validation sets.
![Image](https://github.com/user-attachments/assets/c5efb393-f82c-4fc5-aaf4-f112dfef8733)

- Confusion Matrix: Visualizes the confusion matrix for model predictions.
![Image](https://github.com/user-attachments/assets/60a7dbaa-eec1-4f4f-a9bb-71db117420a2)

- Classification Report: Provides precision, recall, and F1-score for each class.
<img width="839" alt="Image" src="https://github.com/user-attachments/assets/60b9c569-bfd0-4b7d-b809-88821e5e7245" />

## Testing Samples
![Image](https://github.com/user-attachments/assets/78655a2c-08a2-46ce-afc2-7a21dd0e56ef)

![Image](https://github.com/user-attachments/assets/ef752d8c-a732-401b-80b1-0641c56b904b)
