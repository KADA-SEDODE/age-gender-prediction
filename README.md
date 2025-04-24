# 🧠 Age & Gender Prediction with Deep Learning

> Deep learning project for age and gender prediction from facial images using **PyTorch**, **Google Colab**, and **InceptionV3**.
---

## 🧾 Overview

This project leverages a pre-trained **InceptionV3** model to predict **gender** and analyze **age** from face images.  
We conducted a detailed exploration of hyperparameters such as optimizer, learning rate, dropout rate, and the number of neurons in the dense layers.

> ✅ All the training, evaluation, and visualizations are performed in a **single clean notebook** built with **Google Colab**.

---

## 📁 Files in this repository

- `Projet_Prediction_age_Sexe.ipynb` — Main notebook: training, testing, and visual analysis
- `README.md` — This file

---

## 🔗 Open in Google Colab

👉 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/KADA-SEDODE/age-gender-prediction/blob/main/Projet_Prediction_age_Sexe.ipynb)

---

## 📊 Results

| Metric         | Test Score     |
|----------------|----------------|
| **F1-score**   | **0.92**       |
| Precision      | 0.88           |
| Recall         | 0.96           |

> 🔍 Age regression is being considered for future multitask learning experiments.

---

## ⚙️ Model & Training Details

- **Base model**: InceptionV3 (fine-tuned)
- **Optimizer**: Adam (best performance)
- **Learning rate**: 0.001
- **Dropout rate**: 0.3
- **Dense layer**: 256 neurons
- **Early stopping**: patience = 3

Training was done with:
- Normalized & augmented images
- Train/Val/Test splits
- Early stopping to avoid overfitting

---

## 🗂 Dataset

- **Dataset**: [UTKFace](https://susanqq.github.io/UTKFace/)
- **Size**: 33,488 images
- **Format**: `age_gender_ethnicity_timestamp.jpg`  
  → e.g., `25_0_0_201701161745.jpg` → 25-year-old male

---

## 👥 Authors

- Cristian **BEREGOI**  
- Kokouvi **KADA-SEDODE** *(Marvin)*

🎓 Master MoSEF – Université Paris 1 Panthéon-Sorbonne (2024–2025)  
Supervisors: *Roman Yurchak* & *Coulibaly Amed*

---

## 📜 Quote

> *"Teaching a machine to recognize a face  
is teaching it a piece of how we see the world."*

---

## 📌 License

This repository is distributed for educational and research purposes only.
