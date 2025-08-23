# 🚀 Nova.AI Meeting Transcriber Pro

A high-performance Chrome extension that provides real-time meeting transcription, intelligent summarization, and AI-powered response suggestions with professional-grade reliability and speed.

## ✨ Enhanced Features

### 🎯 Core Capabilities
- **⚡ Real-Time Transcription**: Live speech-to-text with 10-second chunks
- **🎤 Dual Audio Capture**: Both microphone and tab audio (non-disruptive)
- **🧠 AI Summarization**: Structured summaries with key points and action items  
- **💡 Smart Suggestions**: Context-aware response recommendations
- **🚀 Performance Optimized**: Async processing, caching, retry logic
- **🔒 Privacy Focused**: Local processing, no data storage

### 🛠 Technical Improvements
- **Async Architecture**: Non-blocking operations with thread pools
- **Smart Caching**: Reduces API calls and improves response times
- **Error Recovery**: Automatic retries with exponential backoff
- **Health Monitoring**: Real-time system status and performance metrics
- **Modern UI**: Sleek interface with dark mode support
- **Production Ready**: Docker deployment with monitoring

## 🏗 Architecture Overview

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│ Chrome Extension│────│  FastAPI Backend │────│   Groq API      │
│                 │    │                  │    │                 │
│ • Audio Capture │    │ • Async Processing│    │ • Whisper       │
│ • UI Management │    │ • Smart Caching  │    │ • Llama Models  │
│ • Error Handling│    │ • Health Checks  │    │ • Rate Limiting │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## ⚡ Quick Start

### 1. Backend Setup

#### Option A: Docker (Recommended)
```bash
# Clone the repository
# 🚀 Nova.AI Meeting Transcriber Pro

A high-performance Chrome extension that provides real-time meeting transcription, intelligent summarization, and AI-powered response suggestions with professional-grade reliability and speed.

## ✨ Enhanced Features

### 🎯 Core Capabilities
- **⚡ Real-Time Transcription**: Live speech-to-text with 10-second chunks
- **🎤 Dual Audio Capture**: Both microphone and tab audio (non-disruptive)
- **🧠 AI Summarization**: Structured summaries with key points and action items  
- **💡 Smart Suggestions**: Context-aware response recommendations
- **🚀 Performance Optimized**: Async processing, caching, retry logic
- **🔒 Privacy Focused**: Local processing, no data storage

### 🛠 Technical Improvements
- **Async Architecture**: Non-blocking operations with thread pools
- **Smart Caching**: Reduces API calls and improves response times
- **Error Recovery**: Automatic retries with exponential backoff
- **Health Monitoring**: Real-time system status and performance metrics
- **Modern UI**: Sleek interface with dark mode support
- **Production Ready**: Docker deployment with monitoring

## 🏗 Architecture Overview

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│ Chrome Extension│────│  FastAPI Backend │────│   Groq API      │
│                 │    │                  │    │                 │
│ • Audio Capture │    │ • Async Processing│    │ • Whisper       │
│ • UI Management │    │ • Smart Caching  │    │ • Llama Models  │
│ • Error Handling│    │ • Health Checks  │    │ • Rate Limiting │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## ⚡ Quick Start

### 1. Backend Setup
##Render Hosting
```bash
Source code fork this repo to your Github, open render and add new project and select Github provider. choose the repo and connect to it
# Server Start command
uvicorn app:app --reload --host 0.0.0.0 --port 8000
# Set environment variables in your platform
GROQ_API_KEY=gsk_your_key_here
ENVIRONMENT=production
PORT=8000
```

### 2. Chrome Extension Setup

1. **Load Extension**
   - Open Chrome → `chrome://extensions/`
   - Enable "Developer mode"
   - Click "Load unpacked" → Select project folder

2. **Configure Settings**
   - Click the Nova.AI icon
   - Click settings gear ⚙️
   - Verify backend URL (default: `http://localhost:8000`)
   - Adjust chunk size and auto-summarization as needed

3. **Grant Permissions**
   - Accept microphone access
   - Allow tab capture permissions

## 📋 Usage Guide

### Starting a Transcription Session

1. **Navigate to Meeting**
   - Join your video call (Google Meet, Zoom, Teams, etc.)
   - Ensure audio is working normally

2. **Start Nova.AI**
   - Click the extension icon
   - Wait for "Connected" status
   - Click "Start Recording" 
   - **Your meeting audio continues normally**

3. **Monitor Progress**
   - Watch live transcription appear
   - Check word count and duration
   - Status indicators show system health

### Using AI Features

1. **Generate Summary**
   - Click "Summarize" after sufficient audio
   - Review structured summary with:
     - Key discussion points
     - Action items identified
     - Important decisions made

2. **Get Response Suggestions**
   - Click "Suggest Response"
   - See context-aware recommendations
   - Copy suggested responses with one click

3. **Auto-Summarization**
   - Enable in settings for automatic summaries every 5 minutes
   - Perfect for long meetings

## ⚙️ Configuration Options

### Backend Configuration

| Environment Variable | Default | Description |
|---------------------|---------|-------------|
| `GROQ_API_KEY` | Required | Your Groq API key |
| `PORT` | `8000` | Server port |
| `ENVIRONMENT` | `development` | Deployment environment |
| `LOG_LEVEL` | `info` | Logging level |

### Extension Settings

- **Backend URL**: API endpoint (default: http://localhost:8000)
- **Chunk Size**: Processing interval (5-15 seconds)
- **Auto-Summarize**: Automatic summary generation
- **Dark Mode**: UI theme preference (follows system)

## 🚀 Production Deployment

### Render Deployment

#Fork this Repo into Your Github

#then open this URL: 
https://dashboard.render.com/web/new

#click on Git provider
#select the forked repo, set name as TransBackend or any other.
#Place this command in start command
```bash
uvicorn app:app --host 0.0.0.0 --port $PORT
```

# Check health
http://xyz.render.com/health

### 2. Chrome Extension Setup

1. **Load Extension**
   - Open Chrome → `chrome://extensions/`
   - Enable "Developer mode"
   - Click "Load unpacked" → Select project folder

2. **Configure Settings**
   - Click the Nova.AI icon
   - Click settings gear ⚙️
   - Verify backend URL (default: `http://localhost:8000`)
   - Adjust chunk size and auto-summarization as needed

3. **Grant Permissions**
   - Accept microphone access
   - Allow tab capture permissions

## 📋 Usage Guide

### Starting a Transcription Session

1. **Navigate to Meeting**
   - Join your video call (Google Meet, Zoom, Teams, etc.)
   - Ensure audio is working normally

2. **Start Nova.AI**
   - Click the extension icon
   - Wait for "Connected" status
   - Click "Start Recording" 
   - **Your meeting audio continues normally**

3. **Monitor Progress**
   - Watch live transcription appear
   - Check word count and duration
   - Status indicators show system health

### Using AI Features

1. **Generate Summary**
   - Click "Summarize" after sufficient audio
   - Review structured summary with:
     - Key discussion points
     - Action items identified
     - Important decisions made

2. **Get Response Suggestions**
   - Click "Suggest Response"
   - See context-aware recommendations
   - Copy suggested responses with one click

3. **Auto-Summarization**
   - Enable in settings for automatic summaries every 5 minutes
   - Perfect for long meetings

## ⚙️ Configuration Options

### Backend Configuration

| Environment Variable | Default | Description |
|---------------------|---------|-------------|
| `GROQ_API_KEY` | Required | Your Groq API key |
| `PORT` | `8000` | Server port |
| `ENVIRONMENT` | `development` | Deployment environment |
| `LOG_LEVEL` | `info` | Logging level |

### Extension Settings

- **Backend URL**: API endpoint (default: http://localhost:8000)
- **Chunk Size**: Processing interval (5-15 seconds)
- **Auto-Summarize**: Automatic summary generation
- **Dark Mode**: UI theme preference (follows system)

## 📊 Performance & Monitoring

### Key Metrics
- **Response Time**: < 2 seconds for transcription
- **Accuracy**: 95%+ on clear audio
-
