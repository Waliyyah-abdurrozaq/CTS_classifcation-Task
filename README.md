# Cassia Tora Seed Classification Project

## Project Description

This machine learning project focuses on classifying Cassia tora seeds into three categories:

1. Grade A – Processed seeds  
2. Grade B – Unprocessed seeds  
3. Impurities – Foreign or unwanted materials

The objective is to automate seed quality assessment using image classification techniques. The model is trained on a dataset of nearly 3,000 labelled images.

## Dataset

- Total images: ~3,000
- Classes: Grade A, Grade B, Impurities
- Image format: JPEG/PNG
- Organised into class-based folders for training

## Tools and Technologies Used

- Python
- TensorFlow/Keras
- Jupyter Notebook
- NumPy, Pandas
- Matplotlib, Seaborn
- OpenCV (for image preprocessing)

## Project Structure

- `data/`: Contains categorized seed images
- `notebooks/`: Contains Jupyter Notebook with code
- `models/`: Saved model files
- `requirements.txt`: List of Python dependencies
- `README.md`: Project overview

## How to Use

1. Clone this repository
2. Install required libraries using `pip install -r requirements.txt`
3. Open the notebook and follow the steps to preprocess data, train the model, and evaluate it

## Objective

To develop an image-based classification model that helps identify high-quality (processed) and lower-quality (unprocessed) seeds and impurities, thereby reducing manual sorting effects and increasing processing efficiency.

