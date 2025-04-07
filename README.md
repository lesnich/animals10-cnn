# 🧠 Animals-10: CNN with Hyperparameter Optimization

This project uses the **Animals-10** dataset to train a Convolutional Neural Network (CNN) for multi-class image classification, with a focus on **manual and automated hyperparameter optimization** using **Optuna**. The full workflow is implemented in **Google Colab** with PyTorch.

---

## 📁 Dataset
- Contains **10 animal classes**, originally named in **Italian**.
- Class folder names are **translated to English**.
- Data is **automatically split** into:
  - Training set
  - Validation set
  - Test set

---

## 🧠 Model Architecture
- Input image size: **128×128**
- **2–3 Convolutional layers** with ReLU activation
- **MaxPooling** + **Dropout**
- **Fully connected (Dense)** layers:
  - FC(128 or 256 units) → FC(10)
- Final activation: handled via `CrossEntropyLoss`
- Optimizer: **Adam**
- Hyperparameters such as learning rate, dropout, FC size are optimized

---

## 🔁 Hyperparameter Optimization
- **Manual search** using `itertools.product`
- **Automated optimization** with **Optuna**
- Optimized:
  - `learning_rate`
  - `dropout`
  - `fc_units`
  - `num_conv_layers`
- Evaluation based on **validation accuracy**

---

## ⚙️ Training Details
- Epochs: 10 (per trial)
- Batch size: 32
- GPU acceleration (if available)
- Best model is saved as: `best_model.pth`

---

## 📊 Evaluation Metrics
- Accuracy
- F1-score (macro, weighted)
- Precision & Recall
- Confusion Matrix
- Visualized:
  - Loss and Accuracy curves
  - Hyperparameter effects (via `seaborn.pairplot`)

---

## ✅ Final Results
- **Test Accuracy**: ~70.1%
- **Weighted F1-score**: ~69.6%
- Top classes: `spider`, `chicken`, `butterfly`
- Weakest: `cat`, `squirrel`, `cow`

---

## 🚀 How to Run
1. Open the notebook in **Google Colab**
2. Follow the sections:
   - 📦 Dataset loading
   - 🧠 Model building
   - 🔧 Hyperparameter tuning
   - 📊 Evaluation
   - 💾 Model saving
3. (Optional) Upload results or `.pth` to GitHub or Drive

---

Made with ❤️ in Google Colab  
Author: **Sofiia Kolesnichenko**
