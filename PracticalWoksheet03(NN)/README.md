# 🐦 Bird Species Classification using Convolutional Neural Networks (CNNs)

This repository contains all source code, model training scripts, evaluation metrics, and visualizations for a deep learning project aimed at classifying bird species found in the Seattle area using mel spectrograms extracted from bird call recordings.

## 📁 Project Structure

├── Preprocessing-BinaryClassification-Model.ipynb
├── Multi-Class-Model.ipynb
├── Predict-Bird-Species.ipynb
├── bird_spectrograms.hdf5
├── results/
│ ├── model/
│ └── figures/
└── README.md


## 📌 Objectives

- Train a **binary CNN classifier** to distinguish between two bird species with the most samples.
- Develop a **multi-class CNN classifier** to identify 12 different bird species.
- Test and analyze predictions on **external .mp3 bird call recordings**.

## 📊 Dataset

- Source: [Xeno-Canto Birdcall Dataset](https://xeno-canto.org)
- Format: Preprocessed as `bird_spectrograms.hdf5`
- Input Shape: `(128, 517)` mel spectrogram images
- Classes: 12 bird species (e.g., amecro, houspa, sonspa, etc.)

## 🧠 Models

### 1. Binary CNN Classifier
- Architecture: Simple Conv2D layers with max-pooling and sigmoid output
- Objective: Distinguish between two bird species
- Evaluation: Confusion matrix, precision, recall, F1-score

### 2. Multi-Class CNN Classifier
- Architecture: Deep Conv2D layers with batch normalization, dropout, and softmax output
- Objective: Predict among 12 bird species
- Evaluation: Classification report, confusion matrix, and prediction probability visualization

## 🎧 External Test Clips
Three unseen `.mp3` clips were segmented, converted to spectrograms, and used for prediction.
- Predictions included confidence scores for each bird species.
- Visualizations were created for top predicted probabilities per clip.

## 🛠️ Libraries Used

- `TensorFlow / Keras`
- `NumPy`
- `Matplotlib`
- `Librosa`
- `h5py`
- `scikit-learn`

## 📈 Evaluation Metrics

- Accuracy
- Precision, Recall, F1-score (Binary & Multi-class)
- Confusion Matrix
- Softmax Probability Visualizations

## 📷 Visualizations

- Training & Validation Accuracy/Loss plots
- Confusion matrices
- Probability distribution bar plots for external clips


## 🔗 Repository Link

Feel free to explore the code, run the notebooks, and extend the project.

**GitHub Repo:** [Bird Species CNN Classifier](https://github.com/Fariha-shah12/DATA-5322-01-25SQ-Statistical-Machine-Learning-2.git)

---

## 👩‍💻 Author

**Fariha Shah**  
Master's in Data Science, Seattle University  
[LinkedIn](https://www.linkedin.com/in/fariha-shah-2ba015149)

