# Galaxy Morphology Classification using Galaxy Zoo

This project applies deep learning to classify galaxy morphologies using imaging data from the Galaxy Zoo project. The task is framed as a supervised image classification problem, using labeled galaxy images to distinguish between broad morphological classes.

The objective is to demonstrate the application of convolutional neural networks (CNNs) to real astronomical imaging data while following best practices in preprocessing, transfer learning, and evaluation.

---

## Dataset

- **Source:** Galaxy Zoo (citizen science morphology labels)
- **Data type:** Optical galaxy images
- **Labels:** Morphological classes (e.g., spiral vs elliptical)
- **Characteristics:** Diverse galaxy shapes, orientations, and brightness levels with class imbalance

Only publicly available Galaxy Zoo labeled data is used.

---

## Methodology

### Preprocessing
- Image resizing to a fixed resolution
- Pixel normalization
- Data augmentation (random rotations, flips) to improve generalization
- Train/validation split to evaluate performance

### Model
- Convolutional Neural Network based on a **pretrained ResNet-50** architecture
- Transfer learning with frozen backbone layers and fine-tuning of higher layers
- Fully connected classification head adapted to the target classes

### Training
- Supervised training using cross-entropy loss
- Optimization using Adam
- Monitoring of validation performance to reduce overfitting

---

## Evaluation

Model performance is assessed using:
- Classification accuracy
- Confusion matrix on validation data
- Training and validation loss curves

Evaluation focuses on generalization across galaxy morphologies rather than maximizing benchmark scores.

---

## Results

- The model successfully learns morphological features from galaxy images with accuracy of 85.28% 
- Transfer learning improves convergence and stability compared to training from scratch
- Augmentation helps mitigate overfitting on limited labeled data

---


