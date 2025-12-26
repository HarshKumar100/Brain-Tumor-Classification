# Brain Tumor Classification using UNet-CBAM

## Project Overview
This project implements a Deep Learning solution to classify brain tumors from MRI scans. The system utilizes a Convolutional Neural Network (CNN) architecture, specifically a UNet model enhanced with a Convolutional Block Attention Module (CBAM), to categorize images into four distinct classes.

The primary objective is to automate the detection process and provide high-accuracy classification to assist in medical image analysis.

## Dataset Description
The model is trained on a brain tumor MRI dataset consisting of the following four categories:
* **Glioma**
* **Meningioma**
* **Pituitary**
* **No Tumor**

### Directory Structure
The script expects the dataset to be uploaded as a zip file (`dataset.zip`). Upon extraction, the directory structure is organized as follows:
* `dataset/Training/` (contains subfolders for each class)
* `dataset/Testing/` (contains subfolders for each class)

## Technical Architecture
The classification model employs an advanced architecture combining:
1.  **UNet:** Adapted for feature extraction and classification tasks.
2.  **CBAM (Convolutional Block Attention Module):** Integrated to refine features by emphasizing relevant spatial and channel-wise information, improving the model's focus on tumor regions.

## Dependencies
The project relies on the following Python libraries:
* **Python 3.x**
* **TensorFlow (v2.x) & Keras:** For model construction and training.
* **NumPy & Pandas:** For numerical operations and data handling.
* **Matplotlib & Seaborn:** For data visualization and plotting training metrics.
* **Google Colab SDK:** For file handling within the Colab environment.

## Usage Instructions

### 1. Environment Setup
The provided notebook (`Brain_Tumour_Classification.ipynb`) is optimized for Google Colab. It requires GPU acceleration for efficient training.

### 2. Execution Steps
1.  **Initialize Environment:** Open the notebook in Google Colab.
2.  **Upload Data:** Execute the initial cells to upload the `dataset.zip` file. The script handles extraction and directory configuration automatically.
3.  **Data Preprocessing:** The script performs image resizing, normalization, and augmentation using `ImageDataGenerator`.
4.  **Model Training:** Run the training cells to fit the UNet-CBAM model to the training data.
5.  **Evaluation:** The script evaluates the model on the testing set to calculate loss and accuracy.

## Project Outputs
Upon completion of training and evaluation, the system automatically packages the results into a downloadable archive named `brain_tumor_research_results.zip`. This archive contains:

* **Quantitative Metrics:**
    * `per_class_metrics.csv`: Precision, recall, and F1-score for each class.
    * `training_history.csv`: Epoch-wise loss and accuracy data.
    * `dataset_statistics.csv`: Distribution of the dataset.
    * `latex_tables.txt`: Metrics formatted for inclusion in LaTeX research papers.
* **Reports:**
    * `research_summary_report.txt`: A text-based summary of the experiment results.
* **Trained Models:**
    * `best_unet_cbam_model.h5`: The model checkpoint with the highest validation accuracy.
    * `unet_cbam_brain_tumor_classifier.h5`: The final trained model weights.
