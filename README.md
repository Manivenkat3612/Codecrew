# 🎯 Codecubicles – AI-Powered Hiring Platform

An intelligent hiring platform that combines resume parsing, ATS scoring, OmniDimension voice interviews, and ML-based behavioral analysis.

---

## 🚀 Features

- **Resume Parsing & ATS Scoring**: Extract skills and match against job requirements  
- **Skill Match Visualization**: Interactive radar charts showing candidate-job fit  
- **OmniDimension Voice Interviews**: AI-powered behavioral interviews via web widget  
- **Transcript Analysis**: ML-based sentiment and behavior scoring using Google Gemini  
- **Workflow Automation**: n8n integration for post-interview automation  
- **Dual Dashboard**: Separate interfaces for candidates and recruiters  

---

## 🛠 Tech Stack

- **Frontend**: React.js with Chart.js for visualizations, Tailwind CSS for styling  
- **Backend**: Python Flask API with MongoDB  
- **AI Voice**: OmniDimension Web Widget  
- **ML Processing**: spaCy, TextBlob, scikit-learn, Google Generative AI  
- **Workflow**: n8n.io automation (webhook-based)  
- **Database**: MongoDB with PyMongo  
- **File Processing**: PyMuPDF for PDF parsing  

---

## 📋 Prerequisites

1. **OmniDimension Account**: Sign up at [OmniDimension](https://www.omnidim.io/refer/code-cubicle)  
2. **Python 3.8+**  
3. **Node.js 16+**  
4. **MongoDB** (local or Atlas)  
5. **n8n** (optional, for workflow automation)  

---

## ⚡ Quick Start

### 🔹 Backend Setup
```bash
cd backend
pip install -r requirements.txt
python app.py
```

### 🔹 Frontend Setup
```bash
cd frontend
npm install
npm start
```

### 🔹 Environment Configuration

Create a `.env` file in the backend directory with:

```env
MONGODB_URI=your_mongodb_connection_string
FLASK_SECRET_KEY=your_secret_key
N8N_WEBHOOK_URL=your_n8n_webhook_url
N8N_EMAIL_WEBHOOK_URL=your_email_webhook_url
UPLOAD_FOLDER=uploads
MAX_CONTENT_LENGTH=16777216
```

---

## 📁 Project Structure

```
Codecubicles/
├── backend/                 # Flask API
│   ├── app.py              # Main Flask application
│   ├── services/           # Business logic services
│   │   ├── resume_service.py       # Resume parsing & ATS scoring
│   │   ├── scoring_service.py      # ML-based transcript analysis
│   │   └── email_service.py        # Email automation via n8n
│   └── requirements.txt    # Python dependencies
├── frontend/               # React application
│   ├── src/
│   │   ├── pages/          # Page components
│   │   │   ├── LoginPage.js
│   │   │   ├── CandidateDashboard.js
│   │   │   └── RecruiterDashboard.js
│   │   ├── services/       # API integration
│   │   └── App.js          # Main React component
│   ├── package.json        # Node.js dependencies
│   └── tailwind.config.js  # Tailwind CSS configuration
└── README.md               # Project documentation
```

---

## 🔧 API Endpoints

### ✅ Working Endpoints

- `GET /api/health` – Health check  
- `POST /api/parse-resume` – Upload and parse resume  
- `POST /api/calculate-ats-score` – Calculate ATS score  
- `POST /api/analyze-transcript` – Analyze interview transcript  
- `GET /api/candidates` – Get all candidates  
- `GET /api/dashboard/stats` – Get dashboard statistics  
- `POST /api/jobs` – Create job posting  
- `GET /api/jobs` – List all jobs  
- `GET /api/jobs/<job_id>` – Get specific job  
- `POST /api/interview/trigger` – Trigger interview using OmniDimension widget  
- `GET /api/interview/transcript/:call_id` – Get interview transcript  
- `POST /api/email/schedule` – Schedule email automation via n8n  

---

## 👨‍💻 Candidate Dashboard Features

1. **Job Selection** – Browse and select available job postings  
2. **Resume Upload** – Drag-and-drop PDF upload  
3. **ATS Score Display** – Real-time skill matching with radar charts  
4. **OmniDimension Widget** – AI voice interview integration  
5. **Interview Status** – Track interview progress and results  

---

## 🧑‍💼 Recruiter Dashboard Features

1. **Job Management** – Create and manage job postings with skill requirements  
2. **Candidate Overview** – View all candidates and track status  
3. **Dashboard Statistics** – View conversion rates, totals, etc.  
4. **Candidate Details** – ATS scores, behavioral analysis, recommendations  

---

## 📞 OmniDimension Integration

- **Web Widget** – Embedded directly in candidate dashboard  
- **Automatic Triggering** – Appears post ATS-score  
- **Transcript Processing** – Receives data via webhook  
- **Behavioral Analysis** – ML-based scoring of voice responses  

---

## 🔄 Current Workflow

1. Recruiter creates a job with required skills  
2. Candidate selects job and uploads resume  
3. System calculates ATS score and displays skill match  
4. OmniDimension Widget triggers for voice interview  
5. ML engine processes transcript and generates behavioral score  
6. n8n integration triggers automation based on score  
7. Recruiter reviews candidate with both scores  

---


## 🤝 Contributing

1. Fork this repo  
2. Create a new feature branch  
3. Commit and push your changes  
4. Open a Pull Request  

---


## 🆘 Support

For queries or issues:

- 📌 Open an issue in this repository  
- 📧 Contact the development team  

---

**Built with ❤️ using OmniDimension AI Voice Technology**
