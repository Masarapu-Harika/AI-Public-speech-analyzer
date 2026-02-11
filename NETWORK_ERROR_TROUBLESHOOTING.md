# 🔧 "Network Error" Troubleshooting Guide

## ❓ What is the "Network error" message?

When you see "Network error. Please try again." in the web interface, it means the JavaScript frontend couldn't communicate with the Flask backend properly.

## 🔍 Common Causes & Solutions

### 1. Backend Not Running
**Symptom:** "Network error" immediately when clicking analyze
**Solution:** 
```bash
python backend/app.py
```
Make sure you see: `Running on http://127.0.0.1:5000`

### 2. Wrong URL/Port
**Symptom:** "Network error" with connection refused
**Solution:** 
- Open browser to exactly: `http://127.0.0.1:5000`
- NOT `localhost:5000` or other variations

### 3. Audio Processing Error (Most Common)
**Symptom:** "Network error" after uploading audio file
**Cause:** FFmpeg not found or audio format not supported
**Solutions:**
- Try with a simple WAV file first
- Install FFmpeg: `winget install Gyan.FFmpeg`
- Use the recording feature instead of file upload

### 4. File Too Large
**Symptom:** "Network error" with large audio files
**Solution:** 
- Keep audio files under 10MB
- Limit recordings to 2-3 minutes

### 5. Browser Issues
**Symptom:** Intermittent "Network error"
**Solutions:**
- Clear browser cache
- Try incognito/private mode
- Try different browser (Chrome, Firefox, Edge)

## 🛠️ Debugging Steps

### Step 1: Check Browser Developer Tools
1. Press `F12` to open developer tools
2. Go to **Network** tab
3. Try to analyze audio
4. Look for `/analyze` request
5. Click on it to see the actual error

### Step 2: Check Backend Logs
1. Look at the terminal where you ran `python backend/app.py`
2. Check for error messages when you try to analyze
3. Common errors:
   - `FFmpeg not found`
   - `Decoding failed`
   - `Speech recognition timeout`

### Step 3: Test with Simple Audio
1. Use the **Record Live Audio** feature
2. Record just 5-10 seconds of speech
3. If this works, the issue is with your uploaded file

## ✅ Quick Fixes

### Fix 1: Use WAV Files Only
- Convert your audio to WAV format first
- WAV files work without FFmpeg

### Fix 2: Use Recording Feature
- Click "Start Recording" instead of uploading
- This bypasses file format issues

### Fix 3: Restart Everything
```bash
# Stop the backend (Ctrl+C)
# Then restart:
python backend/app.py
```

## 🎯 Specific Error Messages

### "Audio processing failed"
- **Cause:** FFmpeg issue or unsupported format
- **Fix:** Use WAV file or install FFmpeg

### "Could not transcribe audio"
- **Cause:** Audio too quiet, no speech, or poor quality
- **Fix:** Record clearer speech, check microphone

### "Speech recognition timeout"
- **Cause:** Google Speech API timeout
- **Fix:** Try shorter audio clips, check internet

## 🚀 Prevention Tips

1. **Always test with recording first** before uploading files
2. **Keep audio files small** (under 5MB)
3. **Use clear speech** with minimal background noise
4. **Stick to WAV format** for best compatibility

## 📞 Still Having Issues?

If you still get "Network error" after trying these steps:

1. **Check the exact error** in browser developer tools
2. **Try the simple demo**: `python simple_demo.py`
3. **Test with a different audio file**
4. **Restart your computer** (sometimes helps with permissions)

## ✨ Success Indicators

You'll know it's working when:
- ✅ Backend shows: `Running on http://127.0.0.1:5000`
- ✅ Browser loads the interface without errors
- ✅ Recording feature works
- ✅ You get analysis results instead of "Network error"

---

**Remember:** The system IS working - "Network error" is just a communication issue that can be fixed! 🎉