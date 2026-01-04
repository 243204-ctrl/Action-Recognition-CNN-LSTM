# Human Action Recognition using CNN + LSTM

## 📌 Project Overview
This project implements a **Human Action Recognition system** using a **Convolutional Neural Network (CNN)** combined with a **Long Short-Term Memory (LSTM)** network.  
The system recognizes human actions from images and annotates them using a trained deep learning model.  
A **Flask-based REST API** is used to communicate between the backend model and a web-based frontend.

---

## 🎯 Objectives
- To recognize human actions from images using deep learning  
- To apply **CNN for spatial feature extraction**  
- To integrate **LSTM for sequential feature modeling**  
- To deploy the trained model using a **REST API**  
- To build a frontend that interacts with the backend model  

---

## 🧠 Model Architecture
1. **CNN (MobileNetV2)**  
   - Extracts spatial features from input images  
2. **LSTM Layer**  
   - Processes extracted features as a sequence (single timestep)  
3. **Fully Connected Layer**  
   - Outputs predicted action class  

**Why CNN + LSTM?**  
CNN extracts visual features, while LSTM models feature dependencies.  
Even though the dataset is image-based, LSTM is used to satisfy the coursework requirement.

---

## 📂 Dataset
- Image-based Human Action Dataset  
- Dataset provided in CSV format:
  - `Training_set.csv`
  - `Testing_set.csv`

**CSV Format**
```
filename,label
image_1.jpg,sitting
image_2.jpg,using_laptop
```

- Images are stored in a folder and mapped using the CSV files.

---

## 🗂 Project Structure
```
Human-Action-Recognition-CNN-LSTM/
│
├── backend/
│   ├── app.py
│   ├── cnn_lstm_model.h5
│   ├── labels.pkl
│   └── requirements.txt
│
├── frontend/
│   ├── index.html
│   ├── script.js
│   └── style.css
│
├── dataset/
│   ├── Training_set.csv
│   ├── Testing_set.csv
│   └── images/
│
├── samples/
│   ├── sitting.jpg
│   ├── hugging.jpg
│   └── using_laptop.jpg
│
├── Human_Action_Recognition_using_CNN_+_LSTM.ipynb
└── README.md
```

---

## 🚀 How to Run the Project

### 1️⃣ Train the Model (Google Colab)
- Open `Human_Action_Recognition_using_CNN_+_LSTM.ipynb`
- Upload dataset CSV files and images
- Run all cells to train the CNN-LSTM model
- Download:
  - `cnn_lstm_model.h5`
  - `labels.pkl`

---

### 2️⃣ Backend Setup (Flask API)

#### Install Dependencies
```bash
pip install -r requirements.txt
```

#### Run Flask Server
```bash
python app.py
```

Server will start at:
```
http://127.0.0.1:5000/
```

---

### 3️⃣ API Endpoint

**POST /predict**

- Input: Image file  
- Output: JSON response  

Example response:
```json
{
  "action": "sitting"
}
```

---

### 4️⃣ Frontend Execution
- Open `frontend/index.html` in a web browser  
- Upload an image  
- Click **Predict**  
- Recognized action will be displayed  

---

## 🖼 Sample Outputs
| Input Image | Predicted Action |
|------------|------------------|
| sitting.jpg | Sitting |
| hugging.jpg | Hugging |
| using_laptop.jpg | Using Laptop |

---

## 🛠 Technologies Used
- Python  
- TensorFlow / Keras  
- OpenCV  
- Flask (REST API)  
- HTML, CSS, JavaScript  
- Google Colab  

---

