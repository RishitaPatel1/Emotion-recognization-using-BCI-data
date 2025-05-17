# Emotion-recognization-using-BCI-data
This project focuses on classifying human emotions using EEG signals by implementing and comparing different deep learning models: a Convolutional Neural Network (CNN), a Long Short-Term Memory Network (LSTM), and a Hybrid CNN-LSTM model with an Attention mechanism.
---

## 📁 Project Structure

* `eeg_preprocessed/` – Contains raw EEG signals.
* `eeg_features/` – Contains feature-extracted signals (`de_1` to `de_80`).
* `continuous_labels/` – Contains continuous labels for emotion dimensions (e.g., arousal or valence).

---

## 🧠 Models Implemented

* **CNN**: Learns spatial representations from 32x32 feature matrices.
* **LSTM**: Captures temporal dependencies from sequential features.
* **Hybrid CNN-LSTM with Attention**: Combines spatial filtering (CNN) with temporal modeling (BiLSTM + attention mechanism).

---

## 🧪 Key Features

* **Data Preprocessing**:

  * Loads `.mat` EEG datasets and reshapes them to a consistent size (32x32).
  * Normalizes and balances the data using SMOTE.
  * Converts continuous labels into 5 discrete emotion classes: Neutral, Sad, Happy, Fear, Angry.

* **Model Training**:

  * Trains models using `CrossEntropyLoss` and the Adam optimizer.
  * Uses `CosineAnnealingWarmRestarts` scheduler for learning rate tuning.
  * Tracks training/validation loss and evaluates model metrics.

* **Evaluation Metrics**:

  * Accuracy, Precision, Recall, F1-Score, Confusion Matrix.

* **Visualization**:

  * Training and validation loss plots for all models.
  * Comparison plot of validation losses.

---

## 📥 Dataset

This project uses the **SEED-VII** dataset provided by the BCMI Lab at Shanghai Jiao Tong University.

* You can download the dataset from the official website:
  🔗 [https://bcmi.sjtu.edu.cn/home/seed/](https://bcmi.sjtu.edu.cn/home/seed/)

* After downloading, place the dataset contents in the following directory structure:

  ```
  D:/DL_Project/
  ├── eeg_preprocessed/
  ├── eeg_features/
  └── continuous_labels/
  ```

---

## ⚙️ Installation & Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Emotion-recognization-using-BCI-data.git
   cd Seed_BCI_final
   ```

2. Install required packages:

   ```bash
   pip install numpy scipy matplotlib scikit-learn imbalanced-learn torch
   ```

3. Make sure your dataset files are placed correctly (see dataset section above).

---

## 🧾 Usage

1. Run the script:

   ```bash
   python main.py
   ```

2. The script will:

   * Load and preprocess the EEG data.
   * Train and evaluate three models (CNN, LSTM, Hybrid).
   * Print accuracy and other metrics for each model.
   * Show comparison plots of training and validation loss.

---

## 📊 Sample Output (Example)

```text
Training CNN Model...
CNN - Accuracy: 0.8521, Precision: 0.8553, Recall: 0.8521, F1: 0.8520

Training LSTM Model...
LSTM - Accuracy: 0.8147, Precision: 0.8178, Recall: 0.8147, F1: 0.8142

Training Hybrid Model...
Hybrid - Accuracy: 0.8765, Precision: 0.8792, Recall: 0.8765, F1: 0.8760
```

---

## 📂 Output

* Confusion matrices
* Performance metrics for each model
* Training/Validation loss plots
* Comparison of model performance

---

## 👤 Author

**Rishita Patel**
Master’s in Computer Science
University of Colorado Denver

**Nakul Magotra**
Master’s in Computer Science
University of Colorado Denver

---

