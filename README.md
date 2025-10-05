# 🚀 NASA Space Apps Challenge - CSV AI Prediction Platform

<div align="center">

![NASA Space Apps](https://img.shields.io/badge/NASA-Space_Apps_Challenge-0B3D91?style=for-the-badge&logo=nasa)
![React](https://img.shields.io/badge/React-18+-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-4+-000000?style=for-the-badge&logo=express)

**A beautiful space-themed web application for AI-powered data analysis**

Built for [NASA Space Apps Challenge](https://www.spaceappschallenge.org/)

[Live Demo](#) • [Report Bug](https://github.com/hussincode/nasa-project/issues) • [Request Feature](https://github.com/hussincode/nasa-project/issues)

</div>

---

## 🌌 Overview

This project was developed for the NASA Space Apps Challenge, providing an intuitive web interface that allows data scientists and researchers to upload CSV datasets and receive AI-powered predictions.  
The application features a **stunning cosmic-themed UI** that reflects the spirit of space exploration.

### ✨ Key Features
- 🎨 **Immersive Space Theme** – Animated cosmic background with stars and nebulas  
- 📊 **CSV Upload** – Drag-and-drop dataset submission  
- 🤖 **AI Integration** – Seamless connection to machine-learning models  
- ⚡ **Real-time Processing** – Progress bar & live updates  
- 🔄 **Error Handling** – Friendly feedback messages  
- 📈 **Result Visualization** – Classification reports & confusion matrix  
- 🌐 **Responsive Design** – Optimized for all screens  

---

## 🎯 Project Purpose

This application bridges **complex AI models** and **end-users**, making advanced analysis accessible to scientists and analysts working with space data.  
Built specifically for the **NASA Space Apps Challenge**, it showcases how web tech + AI can make predictions **intuitive and inspiring**.

**Target Audience:** Data Scientists, Researchers, Space Data Analysts

---

## 🛠️ Tech Stack

### Frontend
- ⚛️ React 18+
- 🎨 Tailwind CSS (animations + styling)
- 🧩 JavaScript ES6+
- 🌐 Fetch API  

### Backend
- 🟩 Node.js 18+
- ⚙️ Express.js
- 📦 Multer (for file uploads)
- 🌍 Axios + Form-Data  
- 🔐 HTTPS, CORS enabled

### AI Service
- 🧠 Flask + Python 3
- 🧬 Pandas, NumPy, scikit-learn, XGBoost, LightGBM, CatBoost
- 🧱 Ensemble Stacking Model (LogReg meta-model)

---

## 📋 Prerequisites
- Node.js ≥ 18  
- npm ≥ 8  
- Python ≥ 3.8  
- pip  
- Modern web browser  

---

## ⚙️ Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/hussincode/nasa-project.git
cd nasa-project
2️⃣ Backend Setup
bash
Copy code
cd backend
npm install
Dependencies: express, cors, multer, axios, form-data, https

Run backend:

bash
Copy code
node server.js
Runs at http://localhost:5000

3️⃣ AI Service Setup
bash
Copy code
cd python-ai
pip install -r requirements.txt
Example requirements.txt

nginx
Copy code
Flask
flask-cors
pandas
numpy
scikit-learn
xgboost
lightgbm
catboost
Run Flask API:

bash
Copy code
python app.py
Runs at http://localhost:8000/predict

4️⃣ Frontend Setup
bash
Copy code
cd frontend
npm install
npm start
Frontend runs at http://localhost:3000

🔧 Configuration
Backend (backend/server.js)
js
Copy code
const AI_API_URL = 'http://127.0.0.1:8000/predict';
const PORT = 5000;
Optional .env

env
Copy code
PORT=5000
AI_API_URL=http://127.0.0.1:8000/predict
NODE_ENV=development
Frontend (frontend/src/SpiralGalaxy.jsx)
js
Copy code
const response = await fetch('http://localhost:5000/upload-csv', { ... });
🚀 Running the App
Terminal 1 – AI API

bash
Copy code
cd python-ai
python app.py
Terminal 2 – Backend

bash
Copy code
cd backend
node server.js
Terminal 3 – Frontend

bash
Copy code
cd frontend
npm start
Now open 👉 http://localhost:3000

📁 Project Structure
css
Copy code
nasa-project/
├── backend/
│   ├── server.js
│   └── uploads/
├── frontend/
│   └── src/
│       └── SpiralGalaxy.jsx
└── python-ai/
    ├── app.py
    ├── train_model.py
    ├── stacking_model.pkl
    ├── label_encoder.pkl
    └── feature_names.pkl
🔌 API Endpoints
Health Check
bash
Copy code
GET /health
json
Copy code
{
  "status": "healthy",
  "service": "Express Backend",
  "port": 5000,
  "aiApiUrl": "http://127.0.0.1:8000/predict"
}
Upload CSV
bash
Copy code
POST /upload-csv
Body: multipart/form-data (file field)

Success:

json
Copy code
{
  "success": true,
  "data": { "classification_report": {}, "confusion_matrix": [] },
  "filename": "dataset.csv"
}
📊 Usage Guide
Visit http://localhost:3000

Upload or drag a .csv file

Wait for AI analysis progress bar

View animated report with accuracy, F1, confusion matrix

Click “New Analysis” to restart

🎨 UI Highlights
100+ twinkling stars (CSS animations)

Glass-morphism upload card

Gradient progress bars

Animated accuracy meter

Scrollable results section for long reports

🧠 Model Info
Stacking ensemble combining:

XGBoost

CatBoost

LightGBM

Logistic Regression (meta-model)

Outputs classification report, confusion matrix, accuracy, macro avg, weighted avg.

🐛 Troubleshooting
Issue	Cause	Fix
“Cannot connect to AI API”	Flask not running	python app.py
“Failed to fetch”	Wrong port or CORS	Update fetch URL, ensure CORS
Upload fails	Wrong file type	Use .csv ≤ 10 MB
Port 5000 in use	Already occupied	netstat / change PORT
CORS errors	Missing middleware	app.use(cors())

🔒 Production Notes
✅ Enable strict CORS

✅ Remove rejectUnauthorized:false

✅ Use environment variables

✅ Limit file size

✅ Add rate-limiting (express-rate-limit)

🗺️ Roadmap
 Data visualization charts

 Export to PDF

 User login & history

 Multi-file batch uploads

🤝 Contributing
Fork → branch → commit → PR

Follow existing style

Test before submitting

📜 License
MIT License – see LICENSE

👨‍💻 Author
Hussin Hesham

🌐 GitHub @hussincode

💼 LinkedIn

✉️ heshamhussin172@gmail.com

🙏 Acknowledgments
NASA Space Apps Challenge – inspiration

React Community, Express Team, Space enthusiasts

<div align="center">
Built with ❤️ for NASA Space Apps Challenge 2025
Making AI predictions accessible through beautiful, intuitive interfaces.

</div> ```
