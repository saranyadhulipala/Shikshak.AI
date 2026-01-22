# Shikshak.AI - AI-Powered Teacher Training Platform

## 🎯 Overview
Shikshak.AI helps DIET/SCERT administrators generate personalized teacher training modules in 30 seconds using AI, instead of taking 3-6 months manually.

## ✨ Key Features
- **AI-Powered Generation**: GPT-4 generates complete training modules in 30 seconds
- **Smart Clustering**: Analyzes teacher data and groups by competency gaps
- **Multilingual Support**: Hindi (Devanagari) and English
- **PDF Export**: Download professional training modules
- **Analytics Dashboard**: Track usage and insights

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and npm
- Python 3.9+
- OpenAI API Key

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```
Frontend runs on: http://localhost:5173

### Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
```
Backend runs on: http://localhost:8000

### Environment Variables

Create `backend/.env`:
```
OPENAI_API_KEY=your_openai_api_key_here
```

## 📁 Project Structure
```
ShikshaLokam/
├── frontend/           # React + Tailwind frontend
│   ├── src/
│   │   ├── pages/     # Dashboard, Generator, Analytics
│   │   ├── components/
│   │   └── App.jsx
│   └── package.json
├── backend/           # FastAPI backend
│   ├── main.py       # API endpoints
│   ├── ai_service.py # GPT-4 integration
│   ├── pdf_service.py # PDF generation
│   └── requirements.txt
└── README.md
```

## 🎨 Tech Stack
- **Frontend**: React.js, Tailwind CSS, Recharts
- **Backend**: Python FastAPI
- **AI**: OpenAI GPT-4 API
- **PDF**: ReportLab
- **Deployment**: Vercel (frontend) + Railway (backend)

## 🎭 Demo Flow 
1. Open dashboard → See 3 clusters (30 sec)
2. Click "Generate for Cluster A" → Fill form (2 min)
3. Watch AI generate Hindi module live (30 sec)
4. Show generated module on screen (1 min)
5. Download PDF (30 sec)
6. Show analytics (30 sec)

## 📊 Pre-loaded Demo Data
- **Cluster A**: 650 rural teachers, low behavior management scores
- **Cluster B**: 800 urban teachers, high pedagogy, need advanced resources
- **Cluster C**: 550 tribal teachers, multilingual needs, low infrastructure

## 🌐 Deployment

### Frontend (Vercel)
```bash
cd frontend
npm run build
# Deploy to Vercel
```

### Backend (Railway/Render)
- Push to GitHub
- Connect Railway/Render to repository
- Add OPENAI_API_KEY environment variable

## 📝 API Documentation

### POST /api/analyze
Returns pre-loaded cluster data
```json
{
  "clusters": [
    {
      "id": "A",
      "name": "Cluster A",
      "teacher_count": 650,
      "avg_score": 62,
      "primary_need": "Behavior Management"
    }
  ]
}
```

### POST /api/generate
Generate training module
```json
{
  "topic": "FLN",
  "cluster": "A",
  "duration": "2 hours",
  "language": "Hindi"
}
```

### GET /api/analytics
Returns usage statistics

### POST /api/download-pdf
Download module as PDF

## 🎨 Design
- **Primary Color**: Blue (#1E3A8A)
- **Accent Color**: Orange (#F97316)
- **Professional, government-friendly aesthetic**
- **Mobile-responsive design**

## 🧪 Testing
Test all combinations:
- 3 topics × 3 clusters × 2 languages × 3 durations = 54 combinations

## 📄 License
Built for Innovation for Education Equity Hackathon 2026

## 👥 Team
ShikshaLokam Team

---

## ✅ Current Status (January 20, 2026)

### Completed ✓
- [x] Frontend React application with Tailwind CSS
- [x] Dashboard page with 3 teacher clusters
- [x] Training Generator page with AI integration
- [x] Analytics page with charts and metrics
- [x] Backend FastAPI server with all endpoints
- [x] OpenAI GPT-4 integration for module generation
- [x] PDF generation service with ReportLab
- [x] Hindi and English language support
- [x] Responsive design
- [x] API proxy configuration

### Next Steps 🚀
1. **Setup & Test** (Today - Jan 20)
   - Install backend dependencies
   - Add OpenAI API key
   - Test all features locally
   - Fix any bugs

2. **Final Polish** (Jan 21)
   - Test all 54 combinations (3 topics × 3 clusters × 2 languages × 3 durations)
   - Optimize AI prompts for better output
   - Test PDF downloads
   - Prepare demo script

3. **Deployment** (Jan 22 - Deadline)
   - Deploy frontend to Vercel
   - Deploy backend to Railway/Render
   - Final testing
   - Submit to hackathon

4. **Demo Preparation** (Before Feb 5)
   - Practice 5-minute demo
   - Prepare backup plans
   - Test on different devices

### Quick Start
See [SETUP_GUIDE.md](SETUP_GUIDE.md) for detailed setup instructions.

---
**Deadline**: Jan 22, 2026 | **Demo**: Feb 5, 2026

