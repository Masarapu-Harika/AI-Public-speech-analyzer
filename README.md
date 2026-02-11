# AI Public Speaking Feedback System

A Flask-based web application that analyzes speech audio files and provides AI-powered feedback on speaking performance.

## Features

- **Audio-to-Text Conversion**: Converts speech audio to text using Google Speech Recognition
- **Speaking Speed Analysis**: Calculates words per minute (WPM) and provides optimal range feedback
- **Filler Word Detection**: Identifies and counts common filler words (um, uh, like, etc.)
- **Sentiment Analysis**: Analyzes the emotional tone of the speech
- **Personalized Feedback**: Generates actionable recommendations based on analysis results
- **Web Interface**: Clean, responsive UI for easy file upload and result viewing

## Supported Audio Formats

- WAV
- MP3
- FLAC
- M4A

## Installation

1. Clone or download the project files
2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Run the Flask application:
```bash
python app.py
```

4. Open your browser and navigate to `http://localhost:5000`

## Usage

1. Upload an audio file of your speech (max 16MB)
2. Click "Analyze Speech" to process the audio
3. Review the analysis results including:
   - Speaking speed (WPM)
   - Filler word count and breakdown
   - Sentiment analysis
   - Personalized feedback recommendations
4. Read the full transcript of your speech

## Analysis Metrics

### Speaking Speed
- **Optimal Range**: 120-160 words per minute
- **Too Slow**: < 120 WPM
- **Too Fast**: > 180 WPM

### Filler Words
Detects common filler words including:
- um, uh
- like, you know
- so, actually
- basically, literally

### Sentiment Analysis
- **Positive**: Polarity > 0.1
- **Negative**: Polarity < -0.1
- **Neutral**: Polarity between -0.1 and 0.1

## Technical Requirements

- Python 3.7+
- Internet connection (for Google Speech Recognition API)
- Microphone access (if recording directly)

## Project Structure

```
├── app.py                 # Main Flask application
├── templates/
│   └── index.html        # Web interface
├── uploads/              # Temporary audio file storage
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## Future Enhancements

- Real-time audio recording
- Advanced speech metrics (pace variation, pauses)
- Multiple language support
- Export feedback reports
- User accounts and progress tracking
- Integration with presentation slides