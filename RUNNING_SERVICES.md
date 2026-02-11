# 🚀 Currently Running Services

## React Authentication App
- **Status**: ✅ RUNNING
- **URL**: http://localhost:5174/
- **Technology**: React + Vite + Tailwind CSS
- **Features**: Interactive signup, signin, dashboard with animations

## Flask Speech Analysis Backend  
- **Status**: ✅ RUNNING
- **URL**: http://localhost:5000/
- **Technology**: Flask + Python
- **Features**: Speech analysis, interview mode, question relevance analysis

## 🎯 Quick Access Links

### React Auth App
```
http://localhost:5174/
```
**Test Flow:**
1. Signup with your details
2. Signin with credentials  
3. View dashboard
4. Logout and repeat

### Flask Speech Analysis
```
http://localhost:5000/
```
**Features:**
- Audio analysis
- Interview mode with question relevance
- History tracking
- Real-time processing

## 📋 Commands to Manage Services

### React App (Port 5174)
```bash
cd react-auth-app
npm run dev     # Start development server
npm run build   # Build for production
```

### Flask Backend (Port 5000)
```bash
python backend/app.py    # Start Flask server
```

## 🔧 Troubleshooting

### If React app won't start:
```bash
cd react-auth-app
npm install
npm run dev
```

### If Flask backend won't start:
```bash
pip install -r requirements.txt
python backend/app.py
```

### Check running processes:
```bash
netstat -an | findstr :5174  # React app
netstat -an | findstr :5000  # Flask backend
```

## ✅ Current Status: Both services running successfully!