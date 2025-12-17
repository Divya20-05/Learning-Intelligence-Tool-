# 🌐 Web Application - Complete Setup Guide

## ✨ What's New

The Learning Intelligence Tool now has a **beautiful web interface**! Users can upload CSV/JSON files through their browser and get instant predictions with downloadable reports.

---

## 🚀 How to Run the Web App

### Step 1: Navigate to Project
```bash
cd /Users/adityajatling/Documents/Internship_Tools/learning-intelligence-tool
```

### Step 2: Start the Web Server
```bash
python3 app.py
```

**You'll see:**
```
================================================================================
🚀 Learning Intelligence Tool - Web Interface
================================================================================

📍 Server starting at: http://localhost:8080

💡 Instructions:
   1. Open http://localhost:8080 in your browser
   2. Upload a CSV or JSON file with learner data
   3. Get predictions and download reports

================================================================================
```

### Step 3: Open in Browser
Open your web browser and go to:
```
http://localhost:8080
```

---

## 🎨 Web Interface Features

### 1. **Drag & Drop Upload**
- Drag your CSV/JSON file onto the upload area
- Or click "Choose File" to browse
- Instant validation with statistics

### 2. **Automatic Predictions**
- AI predictions run automatically after upload
- See loading indicator with progress
- Results appear in seconds

### 3. **Interactive Results Dashboard**
- **Overview Tab**: Summary stats and risk distribution
- **High-Risk Students Tab**: Students needing intervention
- **Difficult Chapters Tab**: Chapters requiring improvement
- **Key Factors Tab**: Feature importance with visual bars
- **Full Report Tab**: Complete text analysis

### 4. **One-Click Downloads**
- 📄 **JSON Report** - All predictions in JSON format
- 📝 **Text Report** - Human-readable analysis
- 📊 **CSV Reports** - ZIP file with all CSV files

### 5. **Premium Design**
- Beautiful gradient backgrounds
- Smooth animations
- Responsive (works on mobile!)
- Modern, professional look

---

## 📋 Usage Workflow

1. **Start Server**
   ```bash
   python3 app.py
   ```

2. **Upload File**
   - Open http://localhost:5000
   - Upload your CSV/JSON file
   - See validation results

3. **View Predictions**
   - Automatic analysis runs
   - Browse results in tabs
   - See high-risk students
   - Check difficult chapters

4. **Download Reports**
   - Click download buttons
   - Get JSON, Text, or CSV reports
   - Save for later use

5. **Upload Another File**
   - Click "Upload New File"
   - Repeat the process

---

## 🔧 API Endpoints (For Developers)

The web app also provides REST API:

### Upload File
```bash
POST /upload
Content-Type: multipart/form-data
Body: file=<your_file>
```

### Run Predictions
```bash
POST /predict
Content-Type: application/json
Body: {"filename": "upload_20250101_120000.csv"}
```

### Download Report
```bash
GET /download/<output_dir>/json
GET /download/<output_dir>/text
GET /download/<output_dir>/csv
```

---

## 🎯 Two Interfaces Available

### CLI (Command Line)
```bash
learning-intelligence-tool predict -i data/sample_input.csv -f all
```
**Best for:** Automation, scripts, batch processing

### Web Interface
```bash
python3 app.py
# Open http://localhost:5000
```
**Best for:** Interactive use, demos, non-technical users

---

## 🛑 Stopping the Server

Press `Ctrl+C` in the terminal to stop the web server.

---

## 📸 What You'll See

The web interface includes:
- 🎨 Gradient purple header with tool name
- 📤 Large drag-and-drop upload area
- 📊 Statistics cards with data summary
- 📑 Tabbed interface for results
- 💾 Download buttons for reports
- 🔄 "Upload New File" button to reset

---

## ✅ Requirements

All dependencies are already installed:
- Flask (web framework)
- Werkzeug (file handling)
- All ML dependencies

---

**Enjoy the new web interface! 🎉**
