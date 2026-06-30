# ♻️ VisionSort

VisionSort is a deep learning project for automated waste classification using **MobileNetV2** and a custom **Loss-Feedback Cosine Warm Restart Scheduler**. The model classifies waste into 12 different categories to support smart recycling and waste management. :contentReference[oaicite:0]{index=0}

---

## 📌 Features

- 12-class waste image classification
- Transfer Learning with MobileNetV2
- Two-phase training (Frozen Backbone → Fine-tuning)
- Custom Loss-Feedback Cosine Warm Restart Scheduler
- Class-weighted training for imbalanced data
- Model checkpointing and resume support
- Training and validation visualization

---

## 🗂️ Dataset

- **Dataset:** Garbage Classification
- **Source:** Kaggle
- **Total Images:** 15,515
- **Classes:**
  - Battery
  - Biological
  - Brown Glass
  - Cardboard
  - Clothes
  - Green Glass
  - Metal
  - Paper
  - Plastic
  - Shoes
  - Trash
  - White Glass

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- MobileNetV2
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## 📊 Model Performance

| Metric | Value |
|---------|-------|
| Validation Accuracy | **97%** |
| Macro F1 Score | **96%** |
| Weighted F1 Score | **97%** |
| Best Epoch | **16** |

---

## 📈 Training Strategy

- Phase 1: Train classification head
- Phase 2: Fine-tune top MobileNetV2 layers
- AdamW Optimizer
- Label Smoothing
- Early Stopping
- Model Checkpointing
- Adaptive Learning Rate Scheduler

---

## 📷 Results

### Training Curves

- Training Loss decreases consistently.
- Validation Accuracy reaches **97%**.
- Adaptive learning rate improves convergence.

### Confusion Matrix

Most classes achieve high classification accuracy with minor confusion between visually similar classes like plastic and glass.

---

## 📂 Project Structure

```
VisionSort/
│
├── notebook.ipynb
├── README.md
├── checkpoints/
├── images/
├── results/
└── requirements.txt
```

---

## 🚀 Future Improvements

- Deploy using TensorFlow Lite
- Add Grad-CAM visualization
- Improve glass category classification
- Build a web/mobile interface
- Test on real-world recycling images
