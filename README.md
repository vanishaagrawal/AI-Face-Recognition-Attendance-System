# 🎯 AI-Face-Recognition-Attendance-System

A complete **Face Recognition–Based Attendance System** built using **Python**, **OpenCV**, **Dlib**, and **Deep Learning–based facial embeddings**.  
The system automatically detects faces from a live camera feed, recognizes registered users, and marks their attendance in a database.

---

## 📸 Project Overview

This project captures face images of multiple users, extracts facial features using **Dlib’s face recognition model**, and trains a feature database.  
During real-time recognition, the system compares the face embeddings with stored data and marks attendance automatically.

---

## 🔥 Features

- ✔ **Register new users** using live camera (stores face images per user)  
- ✔ **Extract deep face features** using Dlib CNN/ResNet model  
- ✔ **Generate CSV of embeddings** for recognition  
- ✔ **Real-time face detection and recognition**  
- ✔ **Automatically mark attendance** in `attendance.db`  
- ✔ **Tkinter GUI for capturing faces**  
- ✔ **Flask Web UI** (from `app.py`)  
- ✔ **Support for multiple users** (folders like `person_1_name`, `person_2_name`, …)

---

## 🧠 Tech Stack

| Component | Technology Used |
|----------|-----------------|
| **Frontend (Web)** | HTML (inside `templates/`) |
| **GUI** | Tkinter (Python) |
| **Backend** | Python (Flask) |
| **Face Detection** | Dlib + OpenCV |
| **Face Recognition** | Dlib ResNet Model |
| **Database** | SQLite (`attendance.db`) |
| **Environment** | Conda / Virtual Environment |

---

## 📁 Project Structure

```
Face-Recognition-Based-Attendance-System/
│
├── app.py # Flask web app
├── attendance_taker.py # Attendance marking script
├── features_extraction_to_csv.py # Converts face images → embeddings → CSV
├── get_faces_from_camera_tkinter.py # GUI to capture face images
├── requirements.txt # All dependencies
├── attendance.db # SQLite attendance database
├── text_to_write.txt # Internal text logs
├── conda_commands.txt # Instructions to set up environment
├── dlib-19.22.99-cp310-win_amd64.whl # Dlib installation wheel (large file)
│
├── data/
│ ├── data_dlib/
│ │ ├── dlib_face_recognition_resnet_model_v1.dat
│ │ ├── shape_predictor_68_face_landmarks.dat
│ │
│ ├── data_faces_from_camera/
│ │ ├── person_10_keerti/
│ │ │ ├── img_face_1.jpg
│ │ │ ├── img_face_2.jpg
│ │ │ └── ...
│ │ ├── person_11_diksha/
│ │ ├── person_7_vedashree gaikwad/
│ │ ├── person_8_trupthi shetty/
│ │ ├── person_9_vaishnavi salunkhe2/
│ │ └── features_all.csv # Final face embeddings
│
└── templates/
└── index.html # Web interface
```

---

## ⚙️ Installation

### **1️⃣ Create environment**
```
conda create -n face_env python=3.10
conda activate face_env
```

### **2️⃣ Install dependencies**
```
pip install -r requirements.txt
```

### **3️⃣ Install Dlib wheel (provided in repo)**
```
pip install dlib-19.22.99-cp310-cp310-win_amd64.whl
```

---

## 🚀 How to Use

### **1️⃣ Capture faces of new users**
```
python get_faces_from_camera_tkinter.py
```

### **2️⃣ Extract deep-learning features**
```
python features_extraction_to_csv.py
```

### **3️⃣ Run real-time attendance**
```
python attendance_taker.py

```

### **4️⃣ Run the Flask Web App**
```
python app.py
```
Navigate to:
```
http://127.0.0.1:5000
```

---

## 🧪 How Recognition Works

1. Detect face → OpenCV  
2. Locate landmarks → Dlib (68-point model)  
3. Generate embedding → Dlib ResNet (128-D vector)  
4. Compare with stored CSV embeddings  
5. If match found → Mark attendance in SQLite  
6. Update UI and save timestamps

---

## 📊 Database (attendance.db)

Stores:

- Name  
- Date  
- Time  
- Attendance status (Present)

---

## ⚠️ Large Files Notice

GitHub warns because this contains large files such as:

- **shape_predictor_68_face_landmarks.dat (~95MB)**  
- **dlib .whl file**  
- **Face image datasets**

GitHub recommends **Git LFS**, but normal push works.

---

## 📚 Future Improvements

- Add student dashboard  
- Replace SQLite with MySQL  
- Add automatic dataset training pipeline  
- Deploy the Flask app online  
- Automatic face detection from CCTV feed  

---

## 🤝 Contributors

**Vanisha Agrawal**  
B.Tech Computer Science (CSE)

---

## 📄 License

This project is for educational & research purposes.

---

