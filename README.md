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

This project was developed for the NASA Space Apps Challenge, providing an intuitive web interface that allows data scientists and researchers to upload CSV datasets and receive AI-powered predictions. The application features a stunning cosmic-themed UI that reflects the spirit of space exploration.

### ✨ Key Features

- 🎨 **Immersive Space Theme** - Animated cosmic background with stars, nebulas, and shooting stars
- 📊 **CSV Data Upload** - Simple drag-and-drop interface for dataset submission
- 🤖 **AI Integration** - Seamless connection to machine learning prediction models
- ⚡ **Real-time Processing** - Instant feedback with loading states and progress indicators
- 🔄 **Error Handling** - Comprehensive validation and user-friendly error messages
- 📈 **Results Visualization** - Clean display of AI predictions and analysis results
- 🌐 **Responsive Design** - Works seamlessly across desktop and mobile devices

## 🎯 Project Purpose

This application serves as a bridge between complex AI models and end-users, making advanced data analysis accessible to data scientists, researchers, and analysts working on space-related datasets. Built specifically for the NASA Space Apps Challenge, it demonstrates how modern web technologies can make AI predictions intuitive and visually engaging.

**Target Audience:** Data Scientists, Researchers, Space Data Analysts

## 🛠️ Tech Stack

### Frontend
- **React 18+** - Modern UI library with hooks
- **Vanilla CSS** - Custom styling with animations
- **JavaScript ES6+** - Modern JavaScript features
- **Fetch API** - HTTP requests to backend

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Fast, minimalist web framework
- **Multer** - Multipart/form-data file upload handling
- **Axios** - Promise-based HTTP client
- **Form-Data** - Multipart form data encoding

### Integration
- **AI API** - External machine learning model endpoint
- **RESTful Architecture** - Clean API design

## 📋 Prerequisites

Before running this project, ensure you have:

- [Node.js](https://nodejs.org/) v18.0 or higher
- [npm](https://www.npmjs.com/) v8.0 or higher (comes with Node.js)
- Access to the AI prediction API endpoint
- A modern web browser (Chrome, Firefox, Safari, Edge)

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/hussincode/nasa-project.git
cd nasa-project
```

### 2. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Dependencies installed:
# - express: Web server framework
# - cors: Cross-origin resource sharing
# - multer: File upload handling
# - axios: HTTP client
# - form-data: Form data handling
```

### 3. Frontend Setup

```bash
# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install

# Start development server
npm start
```

## 🔧 Configuration

### Backend Configuration

Edit `backend/server.js` to configure your AI API endpoint:

```javascript
// Update this with your AI API URL
const AI_API_URL = 'https://127.0.0.1:8000/predict';

// For HTTP endpoints, use:
// const AI_API_URL = 'http://127.0.0.1:8000/predict';
```

**Port Configuration:**
The backend runs on port 5000 by default. To change:

```javascript
const PORT = 5000; // Change to your preferred port
```

### Frontend Configuration

If you change the backend port, update `frontend/src/SpiralGalaxy.jsx`:

```javascript
const response = await fetch('http://localhost:5000/upload-csv', {
  // Change port number if backend port changed
```

### Environment Variables (Optional)

Create a `.env` file in the backend directory:

```env
PORT=5000
AI_API_URL=https://127.0.0.1:8000/predict
NODE_ENV=development
```

## 🚀 Running the Application

### Development Mode

**Terminal 1 - Backend Server:**
```bash
cd backend
node server.js
```

You should see:
```
🚀 Express Backend Server Started
📡 Server: http://localhost:5000
📤 Upload endpoint: http://localhost:5000/upload-csv
🔍 Health check: http://localhost:5000/health
🤖 AI API: https://127.0.0.1:8000/predict
```

**Terminal 2 - React Frontend:**
```bash
cd frontend
npm start
```

You should see:
```
Compiled successfully!

You can now view the app in the browser.
  Local: http://localhost:3000
```

The application will automatically open in your browser at `http://localhost:3000`.

### Production Build

```bash
cd frontend
npm run build
```

This creates an optimized production build in the `build` folder.

## 📁 Project Structure

```
nasa-project/
├── backend/
│   ├── server.js              # Express server & API routes
│   ├── package.json           # Backend dependencies
│   ├── package-lock.json
│   └── uploads/               # Temporary file storage (auto-created)
├── frontend/
│   ├── src/
│   │   ├── App.js             # Main React application
│   │   ├── SpiralGalaxy.jsx   # Main component with UI
│   │   ├── index.js           # React entry point
│   │   └── index.css          # Global styles
│   ├── public/
│   │   ├── index.html
│   │   └── favicon.ico
│   ├── package.json           # Frontend dependencies
│   └── package-lock.json
├── README.md                  # This file
└── LICENSE                    # MIT License
```

## 🔌 API Documentation

### Backend Endpoints

#### Health Check
```http
GET /health
```

**Response:**
```json
{
  "status": "healthy",
  "service": "Express Backend",
  "port": 5000,
  "aiApiUrl": "https://127.0.0.1:8000/predict"
}
```

#### Upload CSV File
```http
POST /upload-csv
```

**Request:**
- **Method:** POST
- **Content-Type:** multipart/form-data
- **Body:** File field named `file` with CSV data

**Success Response (200 OK):**
```json
{
  "success": true,
  "data": {
    // AI model response data
  },
  "filename": "dataset.csv"
}
```

**Error Response (400/500):**
```json
{
  "error": "Error message",
  "details": "Detailed error information"
}
```

## 📊 Usage Guide

### Step 1: Prepare Your CSV File
Ensure your CSV file contains the required columns for the AI model.

### Step 2: Upload the File
1. Open the application at `http://localhost:3000`
2. Click the upload area or drag and drop your CSV file
3. The file will be validated (must be .csv format)

### Step 3: Processing
- The file is uploaded to the Express backend
- Backend forwards it to the AI prediction API
- You'll see a loading indicator during processing

### Step 4: View Results
- AI predictions are displayed in a clean, formatted view
- Results can be copied or downloaded for further analysis

## 🎨 UI Components

### Cosmic Background
- **100+ animated stars** with twinkling effects at various speeds
- **5 colorful nebula clouds** with smooth floating animations
- **Shooting stars** that traverse the screen periodically
- Fully responsive design adapting to all screen sizes

### Upload Interface
- **Glass-morphism design** with frosted glass effect
- **File validation** ensuring only CSV files are accepted
- **Loading states** with progress feedback
- **Error handling** with clear, actionable messages
- **Success confirmation** with file details and predictions

## 🐛 Troubleshooting

### Common Issues

#### Backend won't start - "Port 5000 already in use"

**Windows:**
```bash
netstat -ano | findstr :5000
taskkill /PID <PID> /F
```

**Linux/Mac:**
```bash
lsof -ti:5000 | xargs kill -9
```

#### "Cannot connect to AI API"
- Verify the AI API is running and accessible
- Check the `AI_API_URL` in `server.js`
- Ensure firewall isn't blocking the connection
- For HTTPS with self-signed certificates, the code includes `rejectUnauthorized: false`

#### CORS Errors in Browser Console
- Ensure `cors` package is installed: `npm install cors`
- Verify `app.use(cors())` is present in `server.js`
- Check backend is running before starting frontend

#### "Failed to fetch" in Frontend
- Confirm backend server is running on port 5000
- Check the fetch URL in `SpiralGalaxy.jsx` matches backend port
- Open `http://localhost:5000/health` to test backend directly

#### File Upload Fails
- Verify file is actually a CSV (not Excel or other format)
- Check file size isn't too large
- Ensure `uploads/` directory has write permissions

## 🔒 Security Considerations

### For Production Deployment

⚠️ **Important:** Remove development-only settings:

1. **SSL Certificate Validation**
   ```javascript
   // Remove this in production:
   rejectUnauthorized: false
   ```

2. **CORS Configuration**
   ```javascript
   // Update to specific domain:
   app.use(cors({
     origin: 'https://yourdomain.com'
   }));
   ```

3. **Environment Variables**
   - Use `.env` files for sensitive data
   - Never commit API keys or secrets to Git

4. **File Upload Security**
   - Implement file size limits
   - Add virus scanning for uploaded files
   - Validate file content, not just extension

5. **Rate Limiting**
   ```bash
   npm install express-rate-limit
   ```

## 🗺️ Roadmap

- [ ] Add data visualization charts
- [ ] Support multiple file formats (Excel, JSON)
- [ ] Implement user authentication
- [ ] Add prediction history
- [ ] Export results to PDF
- [ ] Batch file processing
- [ ] Real-time prediction updates

## 🤝 Contributing

Contributions are welcome! This project was built for NASA Space Apps Challenge, but improvements are always appreciated.

### How to Contribute

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines

- Write clear, descriptive commit messages
- Follow existing code style and conventions
- Test your changes thoroughly
- Update documentation as needed
- Add comments for complex logic

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Hussin Hesham**

- GitHub: [@hussincode](https://github.com/hussincode)
- LinkedIn: [Hussin Hesham](https://www.linkedin.com/in/hussinhesham/)
- Email: heshamhussin172@gmail.com

## 🙏 Acknowledgments

- **NASA Space Apps Challenge** - For inspiring this project
- **React Community** - For excellent documentation and support
- **Express.js Team** - For the robust backend framework
- **Space Enthusiasts** - For the cosmic design inspiration

## 📞 Support

For questions, issues, or suggestions:

- 📧 Email: heshamhussin172@gmail.com
- 🐛 Issues: [GitHub Issues](https://github.com/hussincode/nasa-project/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/hussincode/nasa-project/discussions)

## 🌟 Show Your Support

If you found this project helpful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 🤝 Contributing to the code

---

<div align="center">

**Built with ❤️ for NASA Space Apps Challenge**

*Making AI predictions accessible through beautiful, intuitive interfaces*

</div>
