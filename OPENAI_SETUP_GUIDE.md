# OpenAI Setup Guide 🤖

## Quick Setup (Recommended)

### 1. Run the Setup Script
```bash
python setup_openai.py
```

This will:
- Install the OpenAI library
- Guide you through API key setup
- Test the connection
- Configure everything automatically

### 2. Get Your OpenAI API Key
1. Go to [OpenAI API Keys](https://platform.openai.com/api-keys)
2. Sign in or create an account
3. Click "Create new secret key"
4. Copy the key (starts with 'sk-')
5. Paste it when prompted by the setup script

### 3. Test the Integration
```bash
python test_openai_chatbot.py
```

## Manual Setup (Alternative)

### 1. Install OpenAI Library
```bash
pip install openai==0.28.1
```

### 2. Create .env File
Create a `.env` file in the project root:
```
OPENAI_API_KEY=sk-your-api-key-here
```

### 3. Test Connection
```bash
python test_openai_chatbot.py
```

## Without OpenAI (Free Option)

The chatbot works perfectly without OpenAI! It will automatically use the built-in intelligent responses. Just start the system normally:

```bash
python start_system.py
```

## Features Comparison

### With OpenAI API Key ✨
- **GPT-powered responses**: More natural and conversational
- **Context awareness**: Remembers conversation history
- **Personalized coaching**: Adapts to your specific situation
- **Dynamic responses**: Never repetitive, always fresh

### Without API Key (Free) 🆓
- **Smart responses**: Pre-built expert knowledge base
- **Instant replies**: No API delays
- **Comprehensive coverage**: All major interview topics
- **Reliable**: Always works, no dependencies

## Cost Information

### OpenAI API Pricing
- **GPT-3.5-turbo**: ~$0.002 per 1K tokens
- **Typical conversation**: $0.001-0.002 per response
- **Monthly estimate**: $5-20 for regular use

### Free Alternative
- **No cost**: Built-in responses are completely free
- **No limits**: Unlimited conversations
- **Full functionality**: All features work without API

## Troubleshooting

### "No module named 'openai'"
```bash
pip install openai==0.28.1
```

### "Invalid API key"
- Check that your key starts with 'sk-'
- Verify the key is correct in your .env file
- Make sure you have credits in your OpenAI account

### "API request failed"
- Check your internet connection
- Verify your OpenAI account has available credits
- The system will automatically fall back to local responses

## Getting Started

1. **Quick start**: `python setup_openai.py`
2. **Test it**: `python test_openai_chatbot.py`  
3. **Run system**: `python start_system.py`
4. **Use chatbot**: Go to Interview Mode and click the 🤖 button

Your interview chatbot is now powered by AI! 🎉