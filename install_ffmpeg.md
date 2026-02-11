# How to Install FFmpeg on Windows

## Method 1: Download and Install Manually

### Step 1: Download FFmpeg
1. Go to https://ffmpeg.org/download.html
2. Click on "Windows" 
3. Click on "Windows builds by BtbN" (recommended)
4. Download the latest release (ffmpeg-master-latest-win64-gpl.zip)

### Step 2: Extract and Setup
1. Extract the downloaded zip file to `C:\ffmpeg`
2. You should have a folder structure like: `C:\ffmpeg\bin\ffmpeg.exe`

### Step 3: Add to PATH
1. Press `Win + R`, type `sysdm.cpl`, press Enter
2. Click "Environment Variables"
3. Under "System Variables", find and select "Path", click "Edit"
4. Click "New" and add: `C:\ffmpeg\bin`
5. Click "OK" on all dialogs

### Step 4: Verify Installation
Open a new Command Prompt and run:
```
ffmpeg -version
```

## Method 2: Using Winget (Windows 10/11)

If you have Windows 10/11 with winget:
```
winget install ffmpeg
```

## Method 3: Portable Installation (Quick Fix)

For a quick solution without system-wide installation:

1. Download ffmpeg.exe from: https://www.gyan.dev/ffmpeg/builds/
2. Place ffmpeg.exe in your project folder
3. Update your Python code to specify the ffmpeg path

## Troubleshooting

If you still get errors after installation:
1. Restart your command prompt/IDE
2. Check if ffmpeg is in PATH: `where ffmpeg`
3. Try restarting your computer

## Alternative: Use WAV files only

If FFmpeg installation is problematic, convert your MP3 to WAV using:
- Online converters (cloudconvert.com, convertio.co)
- VLC Media Player (Media → Convert/Save)
- Audacity (free audio editor)