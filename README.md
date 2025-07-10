
# Seed Image Classification Using Transfer Learning

## Project Overview

This project focuses on building a deep learning model to classify images of seeds into three categories:
- **Processed_Grade A**
- **Unprocessed_Grade B**
- **Impurities**

The classification was done using **Transfer Learning** with **EfficientNetB3** in TensorFlow. The goal was to leverage pre-trained knowledge from ImageNet to create a robust image classifier even with a relatively small custom dataset of ~2,000 images.

---

## Dataset Description

The dataset consists of seed images divided into three folders (based on their classes). To train the model effectively, the dataset was **automatically split** into:
- **Training set**
- **Validation set**
- **Test set**

Each subset maintained the same class structure. The split ratio used was approximately 80% for training, 10% for validation, and 10% for testing.

---

##  Exploratory Data Analysis (EDA)

Before modeling, an analysis of the dataset was done to:
- Understand the distribution of images across the classes
- Visualize sample images from each class

This helped confirm that the dataset was relatively balanced and clean, making it suitable for training a classification model.


