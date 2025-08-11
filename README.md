# Music Composer Classification Using Deep Learning

This project classifies music composers — Bach, Beethoven, Chopin, and Mozart — based on their musical pieces using deep learning techniques such as CNN and LSTM.

---

## Project Overview

The goal is to accurately predict the composer of a given piece of music by extracting features from MIDI files and training neural network models.

---

## Getting Started

Follow these steps to prepare your data, extract features, and train the model.

### 1. Download Dataset from Kaggle

- Go to [Kaggle](https://www.kaggle.com/) and download the dataset from path `blanderbuss/midi-classic-music` to get the zip file `midclassics_filtered.zip`.
- Upload the ZIP file to your Colab environment.

### 2. Unzip and Organize Dataset

- Unzip the dataset into your working directory.
- The dataset should contain folders for each composer (`Bach`, `Beethoven`, `Chopin`, `Mozart`).

### 3. Clean Composer Folders

- Use the provided `clean_composer_folder` function to:
  - Move all MIDI files to the top-level composer folder.
  - Remove any subfolders.
  - Delete non-MIDI files.

This step ensures that each composer folder contains only `.mid` files directly.

### 4. Feature Extraction

- Run the feature extraction script to:
  - Convert MIDI files to audio.
  - Extract MFCC features from the audio.
  - Save the features and labels in a JSON file or CSV for neural network training.

### 5. Load Data and Prepare for Model Training

- Load the extracted features and labels into your environment.
- Prepare train, validation, and test splits.

### 6. Train CNN/LSTM Models

- Build and compile the CNN and/or LSTM models.
- Train the model using the prepared datasets.
- Evaluate model performance using accuracy and other metrics.

---

## How to Use This Project

1. Download and unzip dataset.

2. Upload folders for each composer to your working directory.

3. Run the cleaning function on each composer folder to organize files properly.

4. Execute the feature extraction script to create MFCC datasets.

5. Load the dataset into your training script and train the CNN/LSTM model.

---

## Requirements

- Python 3.x
- Libraries:
  - `librosa`
  - `soundfile`
  - `tensorflow`
  - `tqdm`
  - `numpy`
  - `json`
  - `shutil`
  - `os`
  - `subprocess`
  - `tempfile`

Make sure to install required libraries using pip if not already installed.

---

## Acknowledgments

- MIDI to audio rendering using **TiMidity++**.
- Feature extraction via **Librosa**.
- Deep learning built with **TensorFlow/Keras**.

---

## Future Improvements

- Implement data augmentation techniques to increase dataset size.
- Explore more complex architectures like Transformer models.
- Use additional musical features such as tempo and chords.
- Deploy the trained model as a web service for real-time classification.

---

Feel free to contribute, open issues, or suggest improvements!
