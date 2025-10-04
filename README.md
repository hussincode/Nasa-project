# 🌌 CSV AI Prediction Web Application

A beautiful space-themed web application that allows users to upload CSV files and get AI predictions through an intuitive interface with a stunning cosmic background.

![Project Banner](https://img.shields.io/badge/React-18+-blue) ![Node.js](https://img.shields.io/badge/Node.js-18+-green) ![Express](https://img.shields.io/badge/Express-4+-lightgrey)

## ✨ Features

- 🎨 **Beautiful Space-Themed UI** - Animated cosmic background with stars, nebulas, and shooting stars
- 📁 **CSV File Upload** - Easy drag-and-drop or click-to-upload interface
- 🤖 **AI Integration** - Seamless integration with external AI prediction API
- ⚡ **Real-time Processing** - Instant feedback with loading states
- 🔄 **Error Handling** - Comprehensive error messages and validation
- 📊 **Response Display** - Clean display of AI predictions and results

## 🚀 Tech Stack

### Frontend
- **React** - User interface and component management
- **Vanilla CSS** - Styling with inline styles (no frameworks required)
- **JavaScript ES6+** - Modern JavaScript features

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web server framework
- **Multer** - File upload handling
- **Axios** - HTTP client for AI API communication
- **Form-Data** - Multipart form data handling

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- A running AI prediction API endpoint

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/csv-ai-prediction-app.git
cd csv-ai-prediction-app
```

### 2. Install Backend Dependencies

```bash
cd backend
npm install
```

**Dependencies installed:**
- express
- cors
- multer
- axios
- form-data

### 3. Install Frontend Dependencies

```bash
cd ../frontend
npm install
# or
npm start
```

## ⚙️ Configuration

### Backend Configuration

Edit `backend/server.js` to configure your AI API endpoint:

```javascript
// Change this to your AI API URL
const AI_API_URL = 'https://127.0.0.1:8000/predict';
```

**For HTTP endpoints:**
```javascript
const AI_API_URL = 'http://127.0.0.1:8000/predict';
```

**For HTTPS with self-signed certificates:**
The code already includes `rejectUnauthorized: false` for development. Remove this in production.

### Frontend Configuration

The frontend is pre-configured to connect to `http://localhost:5000/upload-csv`. If you change the backend port, update `frontend/src/SpiralGalaxy.jsx`:

```javascript
const response = await fetch('http://localhost:YOUR_PORT/upload-csv', {
```

## 🏃‍♂️ Running the Application

### Option 1: Run Both Services Separately

**Terminal 1 - Backend Server:**
```bash
cd backend
node server.js
```
Expected output:
```
🚀 Express Backend Server Started
📡 Server: http://localhost:5000
```

**Terminal 2 - React Frontend:**
```bash
cd frontend
npm start
```
Expected output:
```
Compiled successfully!
You can now view the app in the browser.
Local: http://localhost:3000
```

### Option 2: Using npm scripts (Optional)

You can add these scripts to your root `package.json`:

```json
{
  "scripts": {
    "start:backend": "cd backend && node server.js",
    "start:frontend": "cd frontend && npm start",
    "dev": "concurrently \"npm run start:backend\" \"npm run start:frontend\""
  }
}
```

Then install concurrently:
```bash
npm install -D concurrently
```

And run:
```bash
npm run dev
```

## 📁 Project Structure

```
csv-ai-prediction-app/
├── backend/
│   ├── server.js           # Express server
│   ├── package.json        # Backend dependencies
│   └── uploads/            # Temporary file storage (auto-created)
├── frontend/
│   ├── src/
│   │   ├── App.js          # Main React app
│   │   ├── SpiralGalaxy.jsx # Main component with UI and upload
│   │   └── index.js        # React entry point
│   ├── public/
│   └── package.json        # Frontend dependencies
└── README.md
```

## 🔌 API Endpoints

### Backend Endpoints

#### Health Check
```
GET http://localhost:5000/health
```
Returns backend and AI API health status.

#### Upload CSV
```
POST http://localhost:5000/upload-csv
```
**Request:**
- Method: POST
- Content-Type: multipart/form-data
- Body: CSV file with key 'file'

**Response:**
```json
{
  "success": true,
  "data": {
    // AI API response data
  },
  "filename": "data.csv"
}
```

## 🎨 UI Components

### Cosmic Background
- **100+ animated stars** with pulsing effects
- **5 nebula clouds** with floating animations
- **Shooting stars** across the screen
- Responsive design for all screen sizes

### Upload Card
- Glass-morphism design
- Drag-and-drop support
- File validation (CSV only)
- Loading states
- Error handling
- Success feedback with AI response display

## 🔒 Security Notes

⚠️ **Important for Production:**

1. **Remove `rejectUnauthorized: false`** from `server.js` if not using self-signed certificates
2. **Update CORS settings** to allow only your frontend domain:
   ```javascript
   app.use(cors({
     origin: 'https://yourdomain.com'
   }));
   ```
3. **Add rate limiting** to prevent abuse
4. **Validate file size** and type on both frontend and backend
5. **Use environment variables** for sensitive configuration

## 🐛 Troubleshooting

### Backend Issues

**"Port 5000 already in use"**
```bash
# Windows
netstat -ano | findstr :5000
taskkill /PID <PID> /F

# Linux/Mac
lsof -ti:5000 | xargs kill -9
```

**"Cannot connect to AI API"**
- Ensure the AI API is running
- Check the AI_API_URL is correct
- Verify firewall settings

### Frontend Issues

**"Failed to fetch"**
- Ensure backend is running on port 5000
- Check browser console for CORS errors
- Verify the fetch URL in SpiralGalaxy.jsx

**CORS Errors**
- Make sure `cors` is installed in backend
- Check `app.use(cors())` is present in server.js

## 📝 Usage

1. Open the application at `http://localhost:3000`
2. Click the upload area or drag and drop a CSV file
3. Wait for the file to be processed
4. View AI predictions in the results section

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Your Name** - *Initial work* - [YourGitHub](https://github.com/yourusername)

## 🙏 Acknowledgments

- Inspired by cosmic designs and space exploration
- React community for excellent documentation
- Express.js for robust backend framework

## 📧 Contact

Project Link: [https://github.com/yourusername/csv-ai-prediction-app](https://github.com/yourusername/csv-ai-prediction-app)

---

Made with ❤️ and ☕
