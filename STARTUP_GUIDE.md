# 🚀 Speech Analyzer System - Startup Guide

## Quick Start Options

### Option 1: Windows Batch Script (Recommended for Windows)
```bash
# Double-click or run from command prompt
START_REACT_SYSTEM.bat
```

### Option 2: Python Script (Cross-platform)
```bash
python start_system.py
```

### Option 3: Manual Startup
```bash
# Terminal 1 - Backend
python backend/app.py

# Terminal 2 - Frontend (in new terminal)
cd speech-analyzer-frontend
npm run dev
```

## 🔧 Prerequisites

- **Python 3.7+** with pip
- **Node.js 16+** with npm
- **Git** (for cloning)

## 📦 First Time Setup

1. **Install Python dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Install Node.js dependencies:**
   ```bash
   cd speech-analyzer-frontend
   npm install
   cd ..
   ```

3. **Create demo user (optional):**
   ```bash
   python create_demo_user.py
   ```

## 🌐 Access URLs

- **Frontend (React):** http://localhost:5173
- **Backend API:** http://localhost:5000

## 👤 Demo Credentials

- **Email:** demo@example.com
- **Password:** demo123

## 🔍 Troubleshooting Network Errors

### If you get "Network error" when signing in:

1. **Check if backend is running:**
   ```bash
   # Test backend connection
   python test_localhost_signin.py
   ```

2. **Restart services:**
   ```bash
   # Stop all processes (Ctrl+C in terminals)
   # Then restart using any startup option above
   ```

3. **Check ports:**
   - Backend should be on port 5000
   - Frontend should be on port 5173
   - Make sure no other services are using these ports

4. **Reset demo user:**
   ```bash
   python create_demo_user.py
   ```

## 🛠️ Common Issues & Solutions

### "Python not found"
- Install Python from https://python.org
- Make sure Python is in your PATH

### "Node.js not found"
- Install Node.js from https://nodejs.org
- Make sure Node.js and npm are in your PATH

### "Port already in use"
- Kill processes using ports 5000 or 5173
- Or change ports in configuration files

### "Database errors"
- Delete `backend/app.db` and restart
- Run `python create_demo_user.py` to recreate demo user

### "CORS errors"
- Make sure backend is running on localhost:5000
- Check browser console for specific error messages

## 📁 Project Structure

```
speech-analyzer/
├── backend/                 # Flask API server
│   ├── app.py              # Main backend application
│   ├── routes/             # API routes
│   ├── models/             # Database models
│   └── services/           # Business logic
├── speech-analyzer-frontend/ # React frontend
│   ├── src/                # React source code
│   ├── package.json        # Node.js dependencies
│   └── vite.config.js      # Vite configuration
├── START_REACT_SYSTEM.bat  # Windows startup script
├── start_system.py         # Cross-platform startup script
└── requirements.txt        # Python dependencies
```

## 🔄 Development Workflow

1. **Start system** using any startup option
2. **Make changes** to code
3. **Frontend auto-reloads** (Vite hot reload)
4. **Backend auto-reloads** (Flask debug mode)
5. **Test changes** in browser

## 🚨 Emergency Reset

If everything breaks:

```bash
# 1. Stop all processes
# 2. Delete database
rm backend/app.db

# 3. Reinstall dependencies
pip install -r requirements.txt
cd speech-analyzer-frontend
npm install
cd ..

# 4. Recreate demo user
python create_demo_user.py

# 5. Restart system
python start_system.py
```

## 📞 Support

If you continue to have issues:

1. Check the terminal outputs for error messages
2. Run the test scripts to diagnose issues
3. Ensure all prerequisites are properly installed
4. Try the emergency reset procedure above

---

**Happy coding! 🎤✨**