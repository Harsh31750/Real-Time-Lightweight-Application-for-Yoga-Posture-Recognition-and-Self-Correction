🧘 Real-Time Lightweight Application for Yoga Posture Recognition and Self-Correction

A real-time yoga posture recognition and correction system built using computer vision and lightweight deep learning. The app is designed to help practitioners, especially beginners, improve their yoga accuracy and safety by providing instant, intelligent feedback through a responsive user interface.

---

📊 Abstract

This application implements a real-time posture analysis and correction pipeline based on "MediaPipe" pose estimation and a lightweight "Convolutional Neural Network (CNN)" model. By analyzing webcam footage and comparing it with ideal poses using a "k-Nearest Neighbors (k-NN)" approach, it computes body joint angles and offers real-time corrective feedback for six common yogasanas.

---

📑 Key Features

* ⌚ "Real-time pose detection" using webcam
* 🧠 "Deep learning-based classification" of six yoga asanas
* 🔄 "Pose correction" by comparing joint angles with ideal postures
* ⏳ "Lightweight model" deployable without GPU
* 📉 "High accuracy": \~98.1% (CNN-based model)
* 🌍 "Browser-based UI" using React and Socket.IO

---

🤷 Asanas Supported

1. Padmasana
2. Tadasana
3. Savasana
4. Trikonasana
5. Bhujangasana
6. Janu Sirsasana

---

📊 Architecture

1. Pose Estimation & Feature Extraction

* Input: User webcam video
* Extract 33 pose keypoints using "MediaPipe" (x, y, z, visibility)
* Total features per frame: 133

2. Lightweight CNN for Classification

* Conv1D + MaxPooling1D layers
* Flatten + Dense layers
* Dropout for regularization
* Trained on 80/20 split of dataset (98k+ frames)

3. Pose Correction with k-NN

* Extracted frame compared with ideal dataset (using k=7)
* Calculate angle deviation for 9 joint angles
* If deviation > 10°, show correction alert in UI

4. Real-Time Feedback

* Backend: Python + Flask + Socket.IO
* Frontend: React.js + Bootstrap
* Real-time communication ensures instant feedback on posture deviation

---

## 🕹️ Frontend Setup

1. cd my-app
2. npm install
3. npm start

> App will run at [http://localhost:3000](http://localhost:3000)


🚀 Backend Setup

1. cd backend
2. pip install -r requirements.txt
3. python app.py

> Backend available at [http://localhost:5000](http://localhost:5000)

> Note: "venv/" is not uploaded. Please create your own virtual environment.

---

📖 Dataset Info

| Asana          | Videos | Frames |
| -------------- | ------ | ------ |
| Padmasana      | 32     | 21,250 |
| Tadasana       | 18     | 14,222 |
| Savasana       | 17     | 17,641 |
| Trikonasana    | 17     | 16,557 |
| Bhujangasana   | 16     | 15,473 |
| Janu Sirsasana | 12     | 12,975 |

* Verified by yoga experts
* Frame rate: 30 fps

---

🔧 Technology Stack

* Frontend: React.js, React Bootstrap
* Backend: Python, Flask, Socket.IO
* Pose Estimation: MediaPipe
* ML Models: CNN (classification), k-NN (pose matching)

---

🔺 Model Performance

| Asana          | Accuracy | Precision |
| -------------- | -------- | --------- |
| Bhujangasana   | 99%      | 99%       |
| Janu Sirsasana | 97%      | 98%       |
| Padmasana      | 100%     | 100%      |
| Savasana       | 99%      | 98%       |
| Tadasana       | 98%      | 98%       |
| Trikonasana    | 96%      | 97%       |

Overall Accuracy: 98.1%
Overall Precision: 98.3%

---

📈 Real-Time Correction Example

* Calculates 9 joint angles (e.g., elbows, knees, shoulders)
* Shows red highlights in UI when deviation exceeds 10°
* Confidence score for corrections shown in interface

---

🔍 Live Demo

▶️ [Watch Demo on Google Drive](https://drive.google.com/file/d/1NK2MJE_sydwh-uibkGs_6HKA5j0bxy1k/view)

---

😎 Authors

* Kumar Harshit Singh
(Department of Computer Science and Engineering, NIT Silchar, India)
📧 \[[harsh31750@gmail.com](mailto:harsh31750@gmail.com)]
