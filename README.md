# Learning Intelligence Tool  
**AI-Powered Learning Analytics for Course Completion Prediction and Learner Insights**

A production-ready CLI-based ML tool that analyzes learner activity data to predict course completion, detect at-risk students early, and identify difficult chapters that need improvement.

Built to demonstrate real-world ML engineering, not notebook experiments.

Python: 3.8+  
License: MIT  

---

## 📋 Table of Contents
- Overview  
- Why This Is a Tool (Not a Notebook)  
- Features  
- Installation  
- Quick Start  
- Usage  
- Input Format  
- Output Format  
- Model Details  
- Architecture  
- Testing  
- AI Usage Disclosure  
- Project Structure  
- Educational Value  
- License  

---

## 🎯 Overview
The Learning Intelligence Tool is designed for internship platforms, LMS systems, and training programs that need actionable insights, not just dashboards.

It helps mentors and administrators:
- Predict whether students will complete a course  
- Identify dropout risks early  
- Detect chapters causing learning friction  
- Take data-backed corrective action  

Everything runs from the command line. No notebooks. No manual steps.

---

## 🧠 Why This Is a Tool (Not a Notebook)?
This project is intentionally built like production software.

What this means in practice:
- Executable CLI (learning-intelligence-tool)  
- Modular, layered architecture  
- Pre-trained models loaded instantly  
- Deterministic predictions with fixed seeds  
- Multiple output formats (text, JSON, CSV)  
- Unit and integration test coverage  
- Reproducible end-to-end pipeline  

This mirrors how ML systems are actually shipped.

---

## ✨ Features

### 1. Course Completion Prediction
- Binary classification for course completion  
- Completion probability (0–1) per student  
- Random Forest classifier for stable performance  

### 2. Early Dropout Risk Detection
- Identifies students likely to drop out early  
- Risk levels: High, Medium, Low  
- Designed for proactive intervention  

### 3. Chapter Difficulty Detection
- Scores each chapter on a 0–100 difficulty scale  
- Uses dropout rate, time spent, scores, and completion rate  
- Flags chapters that need content improvement  

### 4. Insight Generation
- Human-readable reports  
- Feature importance explanations  
- Summary statistics  
- Actionable recommendations  
- Exportable as text, JSON, and CSV  

---

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher  
- pip  

### Clone the Repository
```bash
git clone <repo-url>
cd learning-intelligence-tool
```

### Create Virtual Environment (Recommended)
```bash
python3 -m venv venv
source venv/bin/activate
# Windows: venv\Scripts\activate
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Install the CLI Tool
```bash
pip install -e .
```

---

## ⚡ Quick Start

### Generate Sample Data
```bash
python scripts/generate_data.py
```

### Train Models
```bash
python train_models.py
```

### Run Predictions
```bash
learning-intelligence-tool predict -i data/sample_input.csv -f all
```

---

## 📖 Usage

### Predict
```bash
learning-intelligence-tool predict --input <file> [options]
```

Options:
- -i, --input  Path to CSV or JSON input  
- -o, --output Output directory  
- -f, --format text | json | csv | all  
- -v, --verbose Enable detailed logging  

### Validate Input
```bash
learning-intelligence-tool validate -i data/sample_input.csv
```

### Analyze (Full Pipeline)
```bash
learning-intelligence-tool analyze -i data/sample_input.csv
```

---

## 📊 Input Format

Required columns:

| Column | Description |
|------|------------|
| student_id | Unique student identifier |
| course_id | Course identifier |
| chapter_order | Chapter sequence number |
| time_spent | Time spent in minutes |
| score | Assessment score (0–100) |
| completion_status | 1 = completed, 0 = not completed |

### Sample CSV
```csv
student_id,course_id,chapter_order,time_spent,score,completion_status
1,101,1,30.5,85.0,1
1,101,2,45.2,90.0,1
2,101,1,25.0,70.0,1
2,101,2,50.0,65.0,0
```

---

## 📤 Output Format

### Text Report
Includes completion stats, risk distribution, difficult chapters, key factors, and recommendations.

### JSON Output
```json
{
  "summary_stats": {
    "total_students": 50,
    "predicted_completions": 38,
    "completion_rate": 76.0,
    "high_risk_count": 5
  }
}
```

### CSV Outputs
- student_predictions.csv  
- high_risk_students.csv  
- chapter_difficulty_analysis.csv  
- completion_feature_importance.csv  
- dropout_feature_importance.csv  

---

## 🤖 Model Details

### Course Completion Predictor
- Algorithm: Random Forest  
- Accuracy: ~85–90%  
- F1 Score: ~0.85  

### Dropout Risk Detector
- Algorithm: Gradient Boosting  
- Optimized for recall  

### Chapter Difficulty Analyzer
Statistical scoring using dropout rate, time spent, score inversion, and completion rate.

---

## 🏗️ Architecture
CLI → Data Ingestion → Preprocessing → Feature Engineering → Inference Engine → Insight Generator → Outputs

---

## 🧪 Testing

Run all tests:
```bash
pytest tests/ -v
```

Coverage:
```bash
pytest tests/ --cov=src --cov-report=html
```

---

## 🤝 AI Usage Disclosure

AI tools were used as productivity aids only.

Used for:
- Documentation refinement  
- Boilerplate generation  

Not used for:
- Core ML logic  
- Feature engineering  
- Model decisions  

All AI-assisted outputs were manually reviewed and validated.

---

## 📁 Project Structure
```
learning-intelligence-tool/
├── src/
├── models/
├── data/
├── tests/
├── scripts/
├── outputs/
├── train_models.py
├── requirements.txt
├── setup.py
├── README.md
└── AI_USAGE_DISCLOSURE.md
```

---

## 🎓 Educational Value
Demonstrates production ML engineering, CLI deployment, modular architecture, testing discipline, and reproducible inference pipelines.

---

## 📝 License
MIT License

AI Kata Submission – Data Science & Machine Learning Internship Assessment
