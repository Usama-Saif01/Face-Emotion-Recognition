<div align="center">
  <h1>🎭 Face Emotion Recognition CNN</h1>
  <p><i>Real-Time Facial Expression Classification using TensorFlow & Keras</i></p>

  <!-- Badges -->
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=Keras&logoColor=white" alt="Keras" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
</div>

<br />

A deep learning project that classifies human facial expressions into 7 distinct emotions using a custom Convolutional Neural Network (CNN). The system is trained on grayscale images and includes a real-time detection module using OpenCV to predict emotions directly from a live webcam feed.
## 🗄️ Dataset

This project was trained using the official [FER-2013 (Facial Expression Recognition)](https://www.kaggle.com/datasets/msambare/fer2013) dataset from Kaggle. The data consists of 48x48 pixel grayscale images of faces, pre-categorized into training and testing directories. 

*(Note: The dataset is not hosted in this repository due to size constraints. To run this notebook locally, download the dataset from Kaggle and update the `train_dir` and `test_dir` absolute paths in the setup cell.)*
---

## ✨ Key Features

* **Custom CNN Architecture 🧠:** A sequential deep learning model featuring 4 Convolutional layers with MaxPooling, ending in a high-density fully connected layer.
* **Real-Time Detection 📷:** Integrates OpenCV (`cv2`) to capture live webcam feeds, detect faces dynamically, and overlay the predicted emotion in real-time.
* **Data Augmentation 🔄:** Utilizes Keras' `ImageDataGenerator` for dynamic rescaling, rotation, zooming, and horizontal flipping to prevent overfitting and improve generalization.
* **Multi-Class Classification 📊:** Accurately maps predictions to 7 core emotions: *Angry, Disgust, Fear, Happy, Sad, Surprise, and Neutral*.

## 🛠️ Technology Stack

* **Machine Learning:** TensorFlow, Keras
* **Computer Vision:** OpenCV (`cv2`)
* **Data Manipulation & Visualization:** NumPy, Matplotlib
* **Environment:** Python 3, Jupyter Notebook

---

## 🧠 Architecture Highlights

The network processes 48x48 pixel grayscale images through a robust feature-extraction pipeline:
1. **Input Layer:** `(48, 48, 1)` standardized grayscale image input.
2. **Conv Blocks:** 4 stacked `Conv2D` layers (32, 64, 128, and 256 filters) with `ReLU` activation, each followed by a `MaxPooling2D(2, 2)` layer to down-sample spatial dimensions.
3. **Classification Head:** `Flatten` layer transitioning into a massive 1000-neuron `Dense` layer, ending with a 7-neuron `Softmax` output for probabilistic classification.
4. **Compilation:** Optimized using the `Adam` optimizer and `categorical_crossentropy` loss.

---

## 🗄️ Dataset

This project was trained using the **FER-2013** (Facial Expression Recognition) dataset. The data consists of 48x48 pixel grayscale images of faces, pre-categorized into training and testing directories. 

*(Note: The dataset is not hosted in this repository due to size constraints. To run this notebook locally, ensure you download the FER-2013 dataset and update the `train_dir` and `test_dir` absolute paths in the setup cell.)*

---

## 🚀 Execution Guide

1. **Install Dependencies:**
   Ensure you have the required Python libraries installed in your environment:
```bash
   pip install tensorflow opencv-python numpy matplotlib

```

2. **Setup the Dataset:**
Download the FER dataset and place it on your machine. Update the directory paths in the notebook to point to your local `train` and `test` folders.
3. **Train the Model:**
Run the Jupyter Notebook cells sequentially to compile the model, train it across 10 epochs, and evaluate its accuracy.
4. **Live Detection:**
Execute the final cell to boot up your webcam and see the model predict emotions in real-time. Press `q` to safely quit the video stream.

---

### 👨‍💻 Author

**Usama Saifullah**
*Information Technology Professional | Machine Learning & Cybersecurity*
🌐 [usamasaifullah.com](https://www.google.com/search?q=https://usamasaifullah.com) | 🔗 [LinkedIn](https://www.google.com/search?q=https://www.linkedin.com/in/usama-saifullah-sethar)
