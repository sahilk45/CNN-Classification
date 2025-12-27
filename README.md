# 🐱🐶 Image Classification using CNN (TensorFlow & Keras)

This project implements a **Convolutional Neural Network (CNN)** to classify images of **cats and dogs** using **TensorFlow and Keras**.  
The model is trained on a large image dataset and evaluated on unseen test images.

---

## 📌 Project Overview

- **Task**: Binary Image Classification (Cat vs Dog)
- **Framework**: TensorFlow & Keras
- **Model Type**: Convolutional Neural Network (CNN)
- **Input Image Size**: `256 × 256 × 3`
- **Output**: Probability score using **Sigmoid activation**
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam

---

## 📂 Dataset

The dataset contains images divided into two classes:

- `Cat`
- `Dog`

Directory structure:

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
👉 [https://your-dataset-link-here](https://www.kaggle.com/datasets/princelv84/dogsvscats)

---

## 🚀 How to Run the Project (Google Colab)

1. Open the notebook in **Google Colab**
2. Upload the dataset zip file
3. Unzip the dataset:

```bash
!unzip archive.zip
```
4.Run all cells sequentially
