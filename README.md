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

- Used three pre-trained models: ResNet-50, EfficientNet-B0, and ViT (Vision Transformer).

- ResNet and EfficientNet used frozen backbones with custom binary heads.

- ViT was fine-tuned end-to-end with a 2-class classifier.

### 5. Training with Early Stopping:

- The model is trained with early stopping to prevent overfitting.

- The best model is saved based on validation loss.

### 6. Evaluation:

- Detailed evaluation with confusion matrices and classification reports.

- Plots for training and validation loss and accuracy over epochs.

### 6. GPU 
This project utilizes the Kaggle Notebook with dual T4 GPUs for accelerated training.

## Methodology 
The methodology involves three main stages: first, data preprocessing with augmentations such as resizing, flipping, and brightness and contrast adjustments to enhance model robustness. Second, setting up pre-trained models (ResNet-50, EfficientNet-B0, and Vision Transformer) with customized classification heads for binary output (Foul or Clean). Finally, training is conducted with early stopping and learning rate scheduling, followed by detailed evaluation using accuracy metrics and confusion matrices.

![Image](https://github.com/user-attachments/assets/f2a48e73-40d9-409d-9614-707321dd5ba1)

## 📊 Results
The results section presents the performance comparison of the three models—ResNet-50, EfficientNet-B0, and Vision Transformer—on the classification task of football tackles (Foul vs. Clean). Evaluation metrics such as accuracy, precision, recall, and F1-score were reported, along with confusion matrices for detailed analysis. The results show that the Vision Transformer outperformed ResNet-50 and EfficientNet-B0 in classifying football tackles, achieving the highest accuracy. These results highlight the effectiveness of transformer-based architectures for complex visual classification tasks.

![Image](https://github.com/user-attachments/assets/f018cb99-32f8-4cbe-b9de-1e1e6cee0183)

## Testing Samples
<img width="528" alt="Image" src="https://github.com/user-attachments/assets/a41d8fe1-bd5d-4cf7-81fa-b42b8324a23c" />
<img width="573" alt="Image" src="https://github.com/user-attachments/assets/7e335d22-6df5-41a3-9849-87ca918dc219" />
