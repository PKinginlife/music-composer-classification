# Music Genre and Composer Classification Using Deep Learning

## Project Overview

This project focuses on classifying classical music compositions by composer using deep learning techniques. Specifically, it predicts the composer of a given MIDI musical score from four famous composers:

- Johann Sebastian Bach
- Ludwig van Beethoven
- Frédéric Chopin
- Wolfgang Amadeus Mozart

Two deep learning approaches are implemented:

- **LSTM-based model:** Uses sequential features extracted from the main melody line.
- **CNN-based model:** Uses piano-roll image representations of the music.

Both models leverage symbolic music processing and provide complementary strengths in classification.

---

## Libraries Used

| Library      | Purpose                     | Logo                                                                                                 |
| ------------ | --------------------------- | ---------------------------------------------------------------------------------------------------- |
| TensorFlow   | Deep Learning framework     | ![TensorFlow](https://img.shields.io/badge/TensorFlow-F34F29?logo=tensorflow&logoColor=white)        |
| PyTorch      | Deep Learning framework     | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)                 |
| NumPy        | Numerical computing         | ![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)                       |
| PrettyMIDI   | MIDI processing             | ![PrettyMIDI](https://img.shields.io/badge/PrettyMIDI-Blue?logo=music)                               |
| miditoolkit  | MIDI processing toolkit     | ![miditoolkit](https://img.shields.io/badge/miditoolkit-Blue?logo=music)                             |
| Matplotlib   | Plotting and visualization  | ![Matplotlib](https://img.shields.io/badge/Matplotlib-F37626?logo=matplotlib&logoColor=white)        |
| scikit-learn | Data preprocessing, metrics | ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white) |

---

## Setup Instructions

### 1. **Clone the repository**

```bash
git clone https://github.com/PKinginlife/music-composer-classification.git
cd music-composer-classification
```

### 2. **Install dependencies**

Make sure you have Python 3.7+ installed. Then run:

```bash
# for jupyter notebook on your local
pip install -r requirements.txt
```

### 3. **Get Dataset**

- The MCC_Dataset folder contains the MIDI files downloaded and unzipped from Kaggle.
- If the dataset folder is missing, you can download the MCC Dataset from [Kaggle](https://www.kaggle.com/) path `blanderbuss/midi-classic-music` and unzip the zipped file `midclassics_filtered.zip` into the MCC_Dataset directory inside the project root.

### 4. **Run the notebooks/scripts**

All code for data processing, model training, and evaluation for both the LSTM and CNN models is consolidated in the notebook.

```bash
jupyter notebook Final_Project_MCC.ipynb
```

You can run the notebook either locally or in Google Colab.

---

## Project Structure

```grapghql
├── MCC_Dataset/               # Dataset folder with MIDI files
├── Final_project_MCC.ipynb    # Notebook for LSTM & CNN composer classification
├── requirements.txt           # Python dependencies
└── README.md                  # This file
```

---

## Conclusion and Future Considerations

Both LSTM and CNN models performed well, each with unique strengths, but there is room for improvement to boost generalization and ballance class performance.
.

### Future Improvements

- Combine CNN and LSTM/Transformer to capture both local motifs and long-range dependencies. s
- Use MIDI-specific augmentations like pitch transposition, tempo scaling, and velocity jitter.
- Include multi-track/polyphonic context to capture richer stylistic cues.
- Add symbolic features such as key signatures, chords, and rhythmic complexity.
- Address class imbalance with balanced loss functions or re-weighted sampling.
- Expand dataset size to improve generalization and reduce overfitting.
- Incorporate musicological metrics (motif similarity, stylistic clustering) beyond accuracy.
- Encode instrumentation features (program numbers, instrument families) for better discrimination.

These steps can help build more robust and meaningful composer classification models.
