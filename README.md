# 🌟 Deep Learning for Deepfake Detection  

Ever wondered how we can tell if a video or image is fake?  
This project builds a **smart deepfake detection system** using multiple deep learning models — all combined into a simple and interactive web application 🚀  

🌐 **Live Demo:** https://ameencaslam-ddp-v4.streamlit.app/  

---

## 🔍 Project Overview  

This project uses a combination of **state-of-the-art deep learning models** to detect deepfake images and videos:  

- 🤖 Xception  
- ⚡ EfficientNet  
- 🌀 Swin Transformer  
- 🔗 Cross Attention  
- 🧠 CNN + Transformer Hybrid  

Each model is trained independently, and their outputs are combined using **ensemble learning** to improve overall accuracy and reliability.  

---

## 💻 Web Application  

The system is deployed as a **user-friendly web app**, making it accessible even to non-technical users.  

### 🖼️ Image Mode  
- Upload an image  
- Detects face automatically  
- Shows predictions from all models  
- Displays confidence scores and feature maps  

### 🎥 Video Mode  
- Upload a video  
- Select number of frames (10–300)  
- Performs frame-by-frame analysis  
- Displays predictions, faces, and statistics  

---

## 📊 Dataset  

The model is trained on a balanced dataset of **20,000 face images**:  

- 🟢 10,000 Real Images  
- 🔴 10,000 Fake Images  

### Sources:  
- DFDC (DeepFake Detection Challenge)  
- FaceForensics++  
- CelebDF-v2  

📥 **Dataset Link:**  
https://www.kaggle.com/datasets/ameencaslam/3body-filtered-v2-10k/settings  

---

## 🛠️ Model Training  

### 📋 Requirements  
- Kaggle account with GPU access  
- Dataset added to Kaggle  

### 🔧 Steps  

1. Use the training scripts:  
```bash
train_xception.py
train_efficientnet.py
train_swin.py
train_cross_attention.py
train_cnn_transformer.py
