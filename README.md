# ⚡ HiredNext — Automated Intelligent Network for Interview Preparation

> An AI-powered voice-based interview simulator that helps you practice, get scored, and land the job.

---

## 📌 Overview

**HiredNext** is an intelligent virtual interview platform that simulates real, voice-based interview scenarios and delivers multi-dimensional feedback on your performance. Whether you're preparing for a general behavioral round or a company-specific technical interview at Google, Meta, or Microsoft — HiredNext has you covered.

On top of interview simulation, an integrated **resume analysis module** evaluates your resume's structure, keyword alignment, and role relevance, giving you an AI-generated score and prescriptive recommendations.

> In user trials, HiredNext demonstrated an average improvement of **18% in mock-interview scores** after just three practice sessions.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎙️ Voice Interview Simulation | AI interviewer speaks questions aloud and listens to your verbal responses in real time |
| 🏢 Company-Specific Tracks | Tailored question sets for Google, Meta, Microsoft, TikTok, Pinterest, Facebook, and more |
| 📊 Multi-Dimensional Scoring | Rated out of 100 across Communication, Technical Awareness, Confidence, and Problem-Solving |
| 📄 Resume Analysis (ATS) | Upload your resume and a job description — get a percentage match and actionable feedback |
| 🕓 Past Sessions | Review all previous interview attempts with scores and detailed feedback |
| 📱 Mobile-Responsive UI | Flutter-based frontend with smooth navigation and minimal learning curve |

---

## 🖥️ Screenshots

> Dashboard — take interviews, check scores, and track progress

![Dashboard](./screenshots/dashboard.png)

> Voice Interview Screen — simulated call UI between AI Interviewer and user

![Interview Call](./screenshots/interview_call.png)

> ATS Resume Tracker — upload resume + job description, get a percentage match

![Resume ATS](./screenshots/ats_tracker.png)

---

## 🏗️ Architecture

HiredNext is built as a **modular, microservices-based platform** with three core components:

```
┌─────────────────────────────────────────────────────────┐
│                    HiredNext Platform                   │
│                                                         │
│  ┌──────────────────────┐  ┌──────────────────────────┐ │
│  │  Voice Interaction   │  │   Assessment & Scoring   │ │
│  │  Engine              │  │   Module                 │ │
│  │                      │  │                          │ │
│  │  • Speech-to-Text    │  │  • Content Analysis      │ │
│  │  • Text-to-Speech    │  │  • Communication Metrics │ │
│  │  • Dialogue Manager  │  │  • Composite Rating /100 │ │
│  └──────────────────────┘  └──────────────────────────┘ │
│                                                         │
│  ┌──────────────────────────────────────────────────┐   │
│  │              Resume Analysis Service             │   │
│  │  • Structural Evaluation                         │   │
│  │  • Keyword & ATS Match                           │   │
│  │  • AI Feedback Generator                         │   │
│  └──────────────────────────────────────────────────┘   │
│                                                         │
│  All services communicate via RESTful APIs              │
│  Frontend: Next.js (Web) + Flutter (Mobile)             │
│  Containerized: Docker / Kubernetes                     │
└─────────────────────────────────────────────────────────┘
```

---

## 🧠 How It Works

### 1. Voice Interview Flow

```
User selects interview type (General / Company-Specific)
        │
        ▼
AI Interviewer speaks question via TTS
        │
        ▼
User responds verbally → captured via ASR (Speech-to-Text)
        │
        ▼
NLP model evaluates:
  ├── Answer relevance & domain knowledge
  ├── Communication clarity & fluency
  ├── Filler word usage & pacing
  └── Confidence indicators
        │
        ▼
Composite score out of 100 generated per session
```

### 2. Resume Analysis Flow

```
User uploads Resume (PDF) + Job Description
        │
        ▼
Structural Evaluation (formatting, completeness, length)
        │
        ▼
Keyword & ATS Match (role requirements vs. resume content)
        │
        ▼
AI Feedback Report + Percentage Match score
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend (Web) | Next.js, React, Tailwind CSS |
| Frontend (Mobile) | Flutter |
| Backend | Node.js / REST APIs |
| AI / NLP | Transformer-based NLP models, ASR, TTS |
| Resume Analysis | LLM-based keyword extraction & ATS scoring |
| Auth | Server-side authentication (Next.js auth actions) |
| Containerization | Docker / Kubernetes |
| Database | Cloud-hosted DB |

---

## 🚀 Getting Started

### Prerequisites

```bash
node >= 18.x
flutter >= 3.x
docker (optional, for containerized deployment)
```

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/hirednext.git
cd hirednext

# Install web dependencies
npm install

# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Environment Variables

Create a `.env.local` file in the root directory:

```env
# Auth
NEXTAUTH_SECRET=your_secret
NEXTAUTH_URL=http://localhost:3000

# AI / Speech APIs
SPEECH_API_KEY=your_key
NLP_API_KEY=your_key

# Database
DATABASE_URL=your_db_url
```

---

## 📱 Flutter (Mobile)

```bash
cd mobile/
flutter pub get
flutter run
```

---

## 📈 Scoring Dimensions

Each interview session is evaluated across four dimensions, aggregated into a score out of 100:

| Dimension | What's Measured |
|---|---|
| 💬 Communication | Clarity, fluency, pacing, filler word usage |
| 🧠 Technical Awareness | Domain knowledge, answer relevance, accuracy |
| 🔍 Problem-Solving | Structured thinking, approach quality |
| 💪 Confidence | Tone, delivery, response completeness |

---

## 🗺️ Roadmap

- [x] Voice-based AI interview simulation
- [x] Company-specific question tracks (Google, Meta, Microsoft, etc.)
- [x] Multi-dimensional scoring out of 100
- [x] ATS Resume analyzer with percentage match
- [x] Past session history & feedback reports
- [ ] Real-time emotion & voice tone analysis
- [ ] Mock interview scheduling
- [ ] Gamification — badges, leaderboards, streaks
- [ ] Expanded company database (beyond tech)
- [ ] Advanced AI resume rewriting suggestions

---

## 👥 Author

Aarush Tiwari

School of Computer Science Engineering and Technology  
**Bennett University**, Greater Noida, UP, India — April 2025

---

## 📄 License

This project is for academic and research purposes.
