# 🧠 Animals-10: Transfer Learning & Fine-Tuning

This project uses the **Animals-10** dataset to perform multi-class image classification based on **Transfer Learning** and **Fine-Tuning** techniques. The full pipeline is implemented in **Google Colab** using **PyTorch**.

---

## 📁 Dataset
- Dataset contains **10 animal classes**, originally named in **Italian**.
- Folder names were **translated to English**.
- Dataset was **automatically split** into:
  - Training
  - Validation
  - Testing

---

## 🔄 Transfer Learning
- Base model: **ResNet50** pre-trained on ImageNet
- Adapted final `fc` layer to match 10 classes
- Initial training: **frozen convolutional base**, only classifier head trained
- Fine-tuning phase:
  - Gradual unfreezing of convolutional layers
  - Learning rate scheduler: `ReduceLROnPlateau`
  - Data augmentation: rotation, flip, brightness adjustments

---

## ⚙️ Training Configuration
- Input image size: **128×128**
- Epochs: 10–20
- Batch size: 32
- Optimizer: **Adam**
- Loss function: `CrossEntropyLoss`
- Model checkpoints saved:
  - Initial: `animal_cnn_model.pth`
  - Best after fine-tuning: `model_best.pth`

---

## 📊 Evaluation
- Accuracy
- F1-score (macro, weighted)
- Confusion matrix
- Visualizations:
  - Training vs validation loss & accuracy
  - Misclassified examples

---

## ✅ Final Results
- **Test Accuracy**: ~95.1%
- **F1-score**: ~95.0%
- Best performance: `spider`, `chicken`, `butterfly`
- Weak classes: `squirrel`, `cow`, `cat`

---

## 🚀 How to Run
1. Open the notebook in **Google Colab**
2. Execute step-by-step:
   - Load and split dataset
   - Load pretrained model
   - Replace final classifier
   - Train, fine-tune and evaluate
   - Save results and model
3. Upload `.pth` files to Drive or GitHub (optional)

---

Made with 💻 in Google Colab  
Author: **Sofiia Kolesnichenko**
