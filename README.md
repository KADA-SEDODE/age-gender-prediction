# age-gender-prediction
Deep learning project for age and gender prediction from facial images using PyTorch and multitask learning.

# 🧠 Age & Gender Prediction from Facial Images

This project aims to build a deep learning model capable of:
- 🧓 Predicting the **age** of a person based on a facial image (regression or classification).
- 🚻 Classifying the **gender** (male/female) from the same image.

The model leverages **transfer learning** and **multitask learning** techniques to perform both tasks simultaneously.

---

## 🗂️ Project Structure


---

## 🧪 Models & Techniques

- ✅ **CNN Backbone**: MobileNetV3 / ResNet18 (pretrained on ImageNet)
- 🔄 **Transfer Learning**: Fine-tuned on facial image dataset
- ⚖️ **Multitask Learning**: One shared encoder, two separate heads (age & gender)
- 🔒 **Regularization**: Dropout, Data Augmentation
- 📉 **Loss**: 
