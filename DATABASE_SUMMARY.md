# 📊 Database Details Summary

## 🗄️ Database Overview

**Database Type**: SQLite  
**Location**: `F:\speech\backend\app.db`  
**Size**: 86,016 bytes (0.08 MB)  
**Last Modified**: January 3, 2026  
**SQLite Version**: 3.45.1  

## 📋 Database Tables

### 1. **Users Table** (`user`)
**Purpose**: Stores user account information  
**Rows**: 9 users  

**Columns**:
- `id` - INTEGER PRIMARY KEY (Auto-increment user ID)
- `email` - VARCHAR(120) (User's email address)
- `first_name` - VARCHAR(50) (User's first name)
- `last_name` - VARCHAR(50) (User's last name)
- `phone` - VARCHAR(20) (Phone number)
- `password_hash` - VARCHAR(255) (Encrypted password)
- `created_at` - DATETIME (Account creation timestamp)
- `is_active` - BOOLEAN (Account status)

**Sample Users**:
- John Doe (john.doe@example.com)
- Sathwika Gedela (sathwikagedela26@gmail.com)
- Jane Smith (jane.smith@example.com)
- Plus 6 more users...

### 2. **Speech Sessions Table** (`speech_session`)
**Purpose**: Stores speech analysis results and session data  
**Rows**: 59 sessions  

**Core Columns**:
- `id` - INTEGER PRIMARY KEY (Session ID)
- `user_id` - INTEGER (Links to user table)
- `transcript` - TEXT (Speech-to-text result)
- `wpm` - FLOAT (Words per minute)
- `fillers` - INTEGER (Number of filler words)
- `sentiment` - FLOAT (Sentiment score)
- `confidence` - INTEGER (Confidence percentage)
- `emotion` - VARCHAR(50) (Detected emotion)
- `created_at` - DATETIME (Session timestamp)

**Analysis Columns**:
- `word_count` - INTEGER (Total words spoken)
- `filler_percentage` - REAL (Percentage of filler words)
- `grammar_score` - REAL (Grammar quality score)
- `vocabulary_diversity` - REAL (Vocabulary richness)
- `unique_words` - INTEGER (Number of unique words)
- `pronunciation_clarity` - REAL (Clarity score)

**Assessment Columns**:
- `engagement_level` - VARCHAR(20) (User engagement)
- `skill_level` - VARCHAR(30) (Speaking skill level)
- `pace_assessment` - TEXT (Speaking pace feedback)
- `filler_assessment` - TEXT (Filler word feedback)
- `grammar_assessment` - TEXT (Grammar feedback)
- `vocabulary_assessment` - TEXT (Vocabulary feedback)
- `tone_assessment` - TEXT (Tone feedback)
- `general_impression` - TEXT (Overall assessment)

**Improvement Columns**:
- `strengths` - TEXT (JSON: User's speaking strengths)
- `improvements` - TEXT (JSON: Areas for improvement)
- `actionable_tips` - TEXT (JSON: Specific tips)
- `grammar_errors` - TEXT (JSON: Grammar error details)

## 📊 Database Statistics

**Total Data**:
- **Users**: 9 registered accounts
- **Sessions**: 59 speech analysis sessions
- **Storage**: ~86 KB total database size

**Sample Session Data**:
- Average WPM: ~145 words per minute
- Common emotions: confident, engaged
- Typical confidence: 85-90%
- Session types: Regular analysis, interview practice

## ⚙️ Configuration

**Database URI**: `sqlite:///F:\speech\backend\app.db`  
**Track Modifications**: False (for performance)  
**Models**: User, SpeechSession (Flask SQLAlchemy)  

## 🔧 How to Check Database Details

### Quick Commands:
```bash
# Basic structure and content
python check_database.py

# Comprehensive details
python check_database_details_comprehensive.py

# User-specific data (when backend is running)
python check_users_database.py
```

### Manual SQLite Access:
```bash
# Open database in SQLite command line
sqlite3 backend/app.db

# Common queries
.tables                          # List all tables
.schema user                     # Show user table structure
SELECT COUNT(*) FROM user;       # Count users
SELECT * FROM user LIMIT 5;     # Show first 5 users
```

### Visual Tools:
- **DB Browser for SQLite** (Free GUI tool)
- **SQLite Studio** (Cross-platform)
- **VS Code SQLite extension**

## 💡 Key Insights

1. **Active System**: 59 sessions show the system is being actively used
2. **User Base**: 9 registered users with proper authentication
3. **Rich Data**: Comprehensive speech analysis with 27 different metrics
4. **Performance**: Small database size indicates efficient storage
5. **Features**: Supports both regular analysis and interview practice modes

## 🚀 Database Health

✅ **Database is healthy and functional**  
✅ **All tables properly structured**  
✅ **User authentication working**  
✅ **Session data being saved correctly**  
✅ **No corruption detected**