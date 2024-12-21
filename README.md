# MedicalExpert-I CNN Model

This repository contains a Convolutional Neural Network (CNN) implementation to classify medical images from the dataset into five categories: `Normal`, `Doubtful`, `Mild`, `Moderate`, and `Severe`.

Features
- Preprocessing of medical images including resizing, grayscale conversion, and normalization.
- Implementation of a CNN model with:
- Three convolutional layers.
- Activation functions using ReLU.
- MaxPooling layers for dimensionality reduction.
- Fully connected dense layers for classification.
- Visualization of test samples and model predictions.
- Evaluation metrics including training accuracy, validation accuracy, and confusion matrix.
Dataset
The dataset must be organized into subfolders, each corresponding to a category (e.g., `Normal`, `Doubtful`, `Mild`, `Moderate`, `Severe`).
Place the dataset in the following directory structure:
```
RESEARCH/DATASET/MedicalExpert-I/
    ├── Normal/
    ├── Doubtful/
    ├── Mild/
    ├── Moderate/
    ├── Severe/
```
Requirements
Install the necessary Python libraries using the following:

```bash
pip install tensorflow keras opencv-python-headless matplotlib sklearn mlxtend
```
How to Run
1. Mount Google Drive to access the dataset.
2. Navigate to the dataset directory.
3. Run the script in Google Colab or any Python environment.
 
Key Steps

1. Dataset Preprocessing:
   - Converts images to grayscale.
   - Resizes them to `256x256`.
   - Normalizes pixel values to the range `[0, 1]`.

2. Model Architecture:
   - 3 convolutional layers with ReLU activation and max pooling.
   - Dropout layer to prevent overfitting.
   - Dense layers for final classification.

3. Model Training:
   - Uses Adam optimizer and categorical crossentropy loss.
   - Trains the model for 100 epochs with a 20% validation split.

4. Evaluation and Visualization:
   - Evaluates the model on the test set.
   - Visualizes training loss, accuracy, and test sample predictions.
   - Generates a confusion matrix.
Outputs
- Trained model saved as `medical_expert.h5`.
- Training and validation loss/accuracy plot saved as `CNN_Model.png`.
- Confusion matrix plotted for test set predictions.
Results
- The model reports test accuracy and loss after evaluation.
- Predictions for individual test samples are displayed with their corresponding ground truth labels.
Notes
- Ensure the dataset is correctly formatted and stored in the specified directory.
- Adjust the number of categories in the code if the dataset structure changes.
