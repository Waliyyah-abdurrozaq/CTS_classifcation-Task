
# Seed Image Classification Using Transfer Learning

## 🧠 Project Overview

This project focuses on building a deep learning model to classify images of seeds into three categories:
- **Processed**
- **Unprocessed**
- **Impurities**

The classification was done using **Transfer Learning** with **EfficientNetB3** in TensorFlow. The goal was to leverage pre-trained knowledge from ImageNet to create a robust image classifier even with a relatively small custom dataset of ~2,000 images.

---

## 📁 Dataset Description

The dataset consists of seed images divided into three folders (based on their classes). To train the model effectively, the dataset was **automatically split** into:
- **Training set**
- **Validation set**
- **Test set**

Each subset maintained the same class structure. The split ratio used was approximately 70% for training, 15% for validation, and 15% for testing.

---

## 🔍 Exploratory Data Analysis (EDA)

Before modeling, an analysis of the dataset was done to:
- Understand the distribution of images across the classes
- Visualize sample images from each class
- Check for imbalance or data quality issues

This helped confirm that the dataset was relatively balanced and clean, making it suitable for training a classification model.

---

## 🧼 Data Preprocessing

Data was preprocessed using the following techniques:
- **Rescaling** image pixel values between 0 and 1
- **Resizing** all images to 300x300 pixels (as required by EfficientNetB3)
- **Data augmentation** applied to the training set, including rotation, zoom, flipping, and shearing to increase model generalization

Separate preprocessing pipelines were applied for training, validation, and test datasets.

---

## 🧠 Model Architecture

The model architecture was based on **EfficientNetB3**, a state-of-the-art convolutional neural network pre-trained on ImageNet. The steps included:
- Loading the EfficientNetB3 model without its top layers
- Adding a **custom classification head** with pooling, batch normalization, dropout, and dense layers
- Setting the base model as **trainable**, to allow fine-tuning of the pretrained weights

This combination allows the model to adapt powerful learned features to the seed image dataset.

---

## 🏋🏽‍♀️ Model Training

The model was compiled and trained using:
- **Categorical cross-entropy loss**
- **Adam optimizer** with a low learning rate
- **Early stopping** to prevent overfitting
- **Model checkpointing** to save the best-performing model

Training was done for up to 20 epochs with real-time validation monitoring.

---

## 📊 Model Evaluation

After training, the model was evaluated on the **test dataset** to measure its performance on unseen data. Evaluation metrics included:
- **Accuracy**
- **Loss**
- **Confusion matrix** (optional)
- **Classification report** (optional)

This step helped confirm that the model generalized well and could distinguish between the three seed classes.

---

## 🖼️ Visualizing Preprocessed Data

To better understand how the model "sees" data, preprocessed and augmented images were visualized before and after feeding into the model.

---

## ✅ Key Takeaways
- **Transfer learning** with EfficientNetB3 is effective for small image datasets.
- Data augmentation significantly improves generalization.
- Freezing and later unfreezing pretrained layers can be a great strategy to balance speed and accuracy.
- Using the right image size (300x300 for EfficientNetB3) is crucial.

---

## 🔧 Future Improvements
- Use a larger or more diverse dataset
- Experiment with other architectures like ResNet or MobileNet
- Perform hyperparameter tuning
- Deploy the model in a web app or mobile interface
