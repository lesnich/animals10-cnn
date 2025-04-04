# 🐾 Animals-10 Classification with CNN

This project uses the **Animals-10** dataset to train a Convolutional Neural Network (CNN) for multi-class image classification. The full workflow is implemented in **Google Colab** using PyTorch.

## 📁 Dataset
- Dataset contains **10 animal classes**, originally named in Italian.
- Class folder names are **translated to English**.
- The data is **automatically split** into:
  - Training set
  - Validation set
  - Test set

## 🧠 Model Architecture
- Input image size: **128×128**
- **3 Convolutional layers** with ReLU activation
- **MaxPooling** after each conv block
- **Dropout** (0.5) to prevent overfitting
- **Flatten** → **Dense(256)** → **Dense(10)**
- Final activation: Softmax (via `CrossEntropyLoss`)
- Optimizer: **Adam** with learning rate = 0.001

## ⚙️ Training Details
- Epochs: 20
- Batch size: 32
- Uses GPU (if available)
- Includes **learning rate scheduler** (ReduceLROnPlateau)

## 📊 Evaluation Metrics
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix
- Training/Validation **loss and accuracy curves** (visualized with `matplotlib`)

## 📦 Output
- Trained model saved as: `animal_cnn_model.pth`
- Evaluation reports and graphs included in the notebook

## 🚀 How to Run
1. Open the notebook in **Google Colab**
2. Follow each section:
   - Data loading and preprocessing
   - Model definition
   - Training and validation
   - Evaluation and visualization
3. Optionally, upload results or model to GitHub

---

Made with 💻 in Google Colab  
Author: **Sofiia Kolesnichenko**
