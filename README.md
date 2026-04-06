# 🌟Deep Learning Approaches for Deepfake Detection🌟  

A powerful and comprehensive **deepfake detection system** implementing multiple deep learning architectures, all packed into a **user-friendly web interface**! 🚀  


---

## 🔍 Project Overview  

This project integrates cutting-edge **deep learning architectures** to detect deepfakes:  
- 🤖 **Xception**  
- ⚡ **EfficientNet**  
- 🌀 **Swin Transformer**  
- 🔗 **Cross Attention**  
- 🧠 **CNN-Transformer**  

Each model is **independently trained** but seamlessly combined in the web app for **ensemble predictions**.  

---

<div align="center">
<img src="https://i.postimg.cc/htYKyS4w/Screenshot-2024-12-16-105744.png" alt="Web App Screenshot" width="800">
<p><i>Example of the interactive web app interface</i></p>
</div>

---

<div align="center">
<img src="https://i.postimg.cc/65wqn5Tf/Screenshot-2024-12-16-105555.png" alt="Ensemble Prediction UI" width="800">
<p><i>Results from multiple models displayed together</i></p>
</div> 

---

<div align="center">
<img src="https://i.postimg.cc/2jn31Bj5/Screenshot-2024-12-16-105636.png" alt="Image Analysis Example" width="800">
<p><i>Image mode with face detection visualization</i></p>
</div>  

---

<div align="center">
<img src="https://i.postimg.cc/K8jZDKbB/Screenshot-2024-12-16-110538.png" alt="Video Analysis Example" width="800">
<p><i>Video mode displaying prediction results</i></p>
</div>  

---

<div align="center">
<img src="https://i.postimg.cc/1zNsbLfz/Screenshot-2024-12-16-110507.png" alt="Cropped Faces Example" width="800">
<p><i>Cropped face samples from video</i></p>
</div>  


---

## 📜 License  

This project is licensed under the **Apache License 2.0**. You are free to use, modify, and distribute the code, provided that the following conditions are met:  

1. **Attribution**: Proper credit must be given to the original authors, along with a copy of the license.  
2. **State of Derivative Works**: Any modifications or derivative works must be clearly identified as such.  
3. **No Liability**: The software is provided "as is," without any warranties or guarantees. The authors are not liable for any damages arising from its use.  

For full terms and conditions, refer to the official [LICENSE.md](LICENSE.md) file.

---

## 📊 Dataset  

The project utilizes a balanced dataset of **20,000 face-cropped images**:  
- 🟢 **10,000 Real Images**  
- 🔴 **10,000 Fake Images**  
- 📚 Sourced from **DFDC**, **FF++**, and **CelebDF-v2**  

📥 **Dataset Link:** [3body-filtered-v2-10k](https://www.kaggle.com/datasets/ameencaslam/3body-filtered-v2-10k/settings)  

---

## 🛠️ Training the Models  

### 📋 Prerequisites  
- A **Kaggle account** with GPU access  
- Add the dataset to your Kaggle account  

### 🔧 Training Steps  
1. Use the provided `train_*.py` files in Kaggle notebooks  
2. Each model has a unique training configuration  
3. General training parameters:  
   ```python
   NUM_EPOCHS = 30  # Default
   BATCH_SIZE = 32  
   IMAGE_SIZE = 224  # Varies by model
   ```  
4. Key configurations:  
   - Optimizer: **AdamW** with weight decay  
   - Scheduler: **ReduceLROnPlateau**  
   - Experiment tracking: **MLflow integration**  

### 🔄 Model Conversion  

Models are converted for **CPU compatibility**:  
- Use the notebook: [DDP-V4-Converter](https://www.kaggle.com/code/ameencaslam/ddp-v4-converter)  
- Download pre-converted models: [DDP-V4-Models](https://www.kaggle.com/datasets/ameencaslam/ddp-v4-models)  

---

## 🌐 Web Application Setup  

### ⚙️ Environment Setup  
1. Create a virtual environment:  
   ```bash
   python -m venv venv  
   source venv/bin/activate  # Linux/Mac  
   venv\Scripts\activate     # Windows  
   ```  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt  
   ```  

### 📂 Application Structure  
```
deepfake-detection-project-v4/  
├── app.py                   # Main Streamlit app  
├── video_processor.py       # Video utilities  
├── feature_visualization.py # Visualize CNN features  
├── data_handler.py          # Data processing  
├── train_*.py               # Training scripts  
└── converted_models/        # Directory for pre-trained models  
```  

### ▶️ Run the Application  
1. Add converted models to the `converted_models/` folder  
2. Start the app:  
   ```bash
   streamlit run app.py  
   ```  

---

## 🖥️ Using the Web Application  

### 🖼️ Image Analysis  
- Upload an image containing a face  
- View:  
  - 📸 **Face detection visualization**  
  - 📊 **Predictions from each model**  
  - 🧠 **Feature maps** (CNN models only)  

### 🎥 Video Analysis  
- Upload a video file  
- Choose the number of frames to analyze (10–300)  
- View:  
  - 🔍 **Frame-by-frame predictions**  
  - 😃 **Detected faces**  
  - 📈 **Confidence scores and stats**  

---

## 💡 Features  

- 🔗 **Multi-model ensemble predictions**  
- 🕵️‍♂️ **Real-time face detection**  
- 🖼️ **Feature map visualization**  
- 📊 **Confidence tracking**  
- 🌑 **Dark theme UI**  

---

## 🏗️ Model Architecture Details  

### Xception 🤖  
- Specialized in **texture analysis**  
- **Input size:** 299x299  

### EfficientNet ⚡  
- **B3 variant**: Efficiency-accuracy balance  
- **Input size:** 300x300  

### Swin Transformer 🌀  
- **Hierarchical feature learning**  
- **Input size:** 224x224  

### Cross Attention 🔗  
- Focuses on **enhanced feature interaction**  
- **Input size:** 224x224  

### CNN-Transformer 🧠  
- **Hybrid model**: Combines local & global feature learning  
- **Input size:** 224x224  

---

## 📋 Requirements  

- Python 3.8+  
- CUDA-compatible GPU (for training)  
- CPU with **8GB+ RAM** (for inference)  

---

## 📝 Notes  

- ⚠️ Models must be **converted** before use in the web app  
- 🖼️ Feature visualization is limited to **CNN-based models**  
- ⏳ Video processing speed depends on frame count  
