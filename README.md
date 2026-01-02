# 🐱🐶 Image Classification (CNN & Transfer Learning)

This project demonstrates **binary image classification (Cat vs Dog)** using **three different deep learning approaches** in **TensorFlow & Keras**, progressing from a **custom CNN** to **Transfer Learning with VGG16**.

---

## 📌 Project Summary

- **Task**: Binary Image Classification (Cat vs Dog)
- **Framework**: TensorFlow & Keras
- **Input Sizes**:
  - Custom CNN: `256 × 256 × 3`
  - VGG16 Models: `150 × 150 × 3`
- **Output**: Sigmoid probability  
  (`0 → Cat`, `1 → Dog`)
- **Loss Function**: Binary Crossentropy

---

## 📂 Dataset

dataset/

│── train/

│ ├── cats/

│ └── dogs/

│
│── test/

│ ├── cats/

│ └── dogs/


- **Training Images**: 20,000  
- **Validation Images**: 5,000  

📎 **Dataset Link**:  
👉 [https://www.kaggle.com/datasets/princelv84/dogsvscats](https://www.kaggle.com/datasets/princelv84/dogsvscats)

---

## 🧠 Models Implemented

### 🔹 1. Custom CNN (From Scratch)
- Built using Conv2D, BatchNormalization, MaxPooling & Dense layers
- Trained directly on raw images
- **Validation Accuracy**: ~78–80%
- Shows limitations of training deep CNNs from scratch on large images

---

### 🔹 2. VGG16 – Feature Extraction
- Pretrained **VGG16 (ImageNet)** used as a frozen feature extractor
- Custom classifier added on top
- **Validation Accuracy**: ~91–92%
- Faster convergence and better performance than custom CNN

---

### 🔹 3. VGG16 – Fine Tuning
- Upper layers of VGG16 unfrozen (`block5` onwards)
- Lower learning rate + Dropout
- **Validation Accuracy**: ~95%
- Best generalization on unseen images

---

## ⚙️ Training Pipeline

- Dataset loaded using `image_dataset_from_directory`
- Batch size: `32`
- Images normalized to `[0,1]`
- Optimizers used:
  - Adam (Custom CNN & Feature Extraction)
  - RMSprop (Fine-Tuning, low LR)

---

## 🧪 Testing on Unseen Images

- Tested on real-world images using OpenCV
- Model successfully predicts unseen cat/dog images

```python
model.predict(image)
# 0 → Cat | 1 → Dog
```
---

## 📌 Key Takeaways

- Transfer Learning significantly outperforms training from scratch
- Freezing pretrained layers prevents overfitting
- Fine-tuning improves validation accuracy
- Lower learning rates are crucial during fine-tuning

---

## 🚀 How to Run (Google Colab)

- Open notebook in Colab
- Upload dataset ZIP
- Unzip dataset:
```python
!unzip archive.zip
```
- Run all cells sequentially
