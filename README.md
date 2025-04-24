# 🧠 Age & Gender Prediction from Facial Images

This project aims to build a deep learning model capable of:
- 🧓 Predicting the **age** of a person from a facial image (regression).
- 🚻 Classifying the **gender** (male/female) from the same image.

The model uses **InceptionV3** as a pretrained backbone, fine-tuned for our dual objective through **multitask learning**.

---

## 🧬 Dataset

We used the [UTKFace dataset](https://susanqq.github.io/UTKFace/), containing 33,488 images. Each image filename encodes:
- Age (0–100)
- Gender (0 = male, 1 = female)

**Example**: `25_0_0_20170116174525125.jpg` ⟶ age 25, male

---

## 🧪 Techniques Used

| Component              | Description                                                         |
|------------------------|---------------------------------------------------------------------|
| 🧠 Model                | InceptionV3 (ImageNet pretrained)                                   |
| 🔄 Transfer Learning    | Fine-tuning the final layers                                         |
| 🔁 Multitask Learning   | Simultaneous regression (age) and classification (gender)           |
| 🧰 Regularization       | Dropout (0.3), Early Stopping (patience = 3), Data Augmentation     |
| 📈 Optimizer            | Adam with learning rate = `0.0007`                                  |
| ⚖️ Loss                 | Combined loss: `0.7 * MSE(age) + BCE(gender)`                       |

---

## 📊 Results

| Metric               | Value        |
|----------------------|--------------|
| 🧠 F1-score (Gender) | **0.9279**   |
| 🎯 MAE (Age)         | **4.46**     |
| 💥 Test Loss         | **0.488**    |

**Final Model Configuration:**
- Fully Connected Layer: 256 neurons
- Dropout: 0.3
- Learning Rate: 0.0007
- Epochs: 15 (early stopped)

---

## 🧪 Model Training Highlights

Training is done using PyTorch and follows:
1. Train loop with early stopping.
2. Validation at each epoch.
3. Final evaluation on the test set.

Losses are visualized for both training and validation sets to check convergence.

---

## ⚙️ Installation

```bash
git clone https://github.com/KADA-SEDODE/age-gender-prediction.git
```



## 👨‍🎓 Authors
- Marvin KADA-SEDODE
- Cristian BEREGOI
(Master MoSEF – Université Paris 1 Panthéon-Sorbonne, 2025)

---

## 📜 License

This project is licensed under the MIT License.
