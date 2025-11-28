# JudgeSim – AI-Powered Virtual Hackathon Judge Simulator  
**Team Name:** Prime Innovators  
**Track:** Open Innovation  
**Status:** Round 1 & Round 2 – Combined Submission  

---

# 🚀 Overview
JudgeSim is an AI-powered virtual judge simulator that helps hackathon teams evaluate and refine their projects *before* submission. By analyzing project abstracts, problem statements, features, and pitch scripts using NLP and rubric-based scoring, JudgeSim predicts how different types of judges might score the project. This enables teams to correct mistakes early, strengthen technical explanations, improve storytelling, and significantly increase their scoring potential.

---

# 🧩 Problem
Hackathon teams often lose marks not because their idea is weak, but because:
- The problem is not clearly framed  
- The impact is poorly articulated  
- Technical justification is incomplete  
- Demo flow is unclear  
- Judges look for different things: Tech, Impact, UX  

Currently, **no tool** helps teams understand how judges think, evaluate, and score.  
This leads to unpredictable outcomes and preventable errors.

---

# 💡 Solution – JudgeSim
JudgeSim introduces three AI-driven judge personas that evaluate projects from different perspectives:

### 🔵 Tech Judge
- Checks technical depth  
- Reviews architecture & feasibility  
- Measures innovation level  

### 🟢 Impact Judge
- Analyzes real-world relevance  
- Checks user benefit & need  
- Measures societal or domain impact  

### 🟠 UX / Design Judge
- Evaluates clarity of explanation  
- Checks demo flow & storytelling  
- Assesses usability and design focus  

JudgeSim generates:
- Persona-wise scoring (0–100)  
- Strengths & weaknesses  
- Missing or unclear elements  
- Recommended improvements  
- Optimized pitch & demo structure  
- Final predicted judge score  

---

# 🛠 Tech Stack
### **Frontend**
- React.js / Next.js  
- Tailwind CSS  
- Chart.js / Recharts (visualization)

### **Backend**
- Node.js + Express  
**or**  
- Python FastAPI  

### **AI / NLP Engine**
- spaCy / NLTK / HuggingFace  
- Text preprocessing  
- Keyword extraction  
- Semantic similarity  
- Rule-based scoring models  
- Persona-weighted evaluation  

### **Database**
- MongoDB / Firebase  

---

# 🧠 System Architecture Diagram

                              ┌──────────────────────────┐
                              │      User Interface      │
                              │ (Web App: React/Next.js) │
                              └──────────────┬───────────┘
                                             │
                                             ▼
                           ┌────────────────────────────────┐
                           │   Backend API (Node.js/FastAPI)│
                           └──────────────┬─────────────────┘
                                          │
                                          ▼
          ┌───────────────────────────────────────────────────────────────┐
          │             NLP Processing & Understanding Layer              │
          │───────────────────────────────────────────────────────────────│
          │ • Text Cleaning & Tokenization                                │
          │ • Keyword Extraction                                          │
          │ • Semantic Analysis (Problem–Solution Mapping)                │
          │ • Feature & Impact Detection                                  │
          │ • Clarity & Storytelling Scoring                              │
          └──────────────┬──────────────────────┬─────────────────────────┘
                         │                      │
                         │                      │
                         ▼                      ▼
        ┌───────────────────────┐    ┌────────────────────────┐
        │    Tech Judge Model   │    │   Impact Judge Model   │
        │───────────────────────│    │────────────────────────│
        │ • Architecture Score  │    │ • Relevance & Need     │
        │ • Feasibility Score   │    │ • Real-World Impact    │
        │ • Technical Depth     │    │ • Innovation Strength  │
        └──────────────┬────────┘    └──────────────┬─────────┘
                       │                            │
                       │                            ▼
                       │              ┌────────────────────────────┐
                       │              │    UX/Design Judge Model   │
                       │              │────────────────────────────│
                       │              │ • Presentation Flow        │
                       │              │ • Usability & Demo Clarity │
                       │              │ • Storytelling Structure   │
                       │              └──────────────┬─────────────┘
                       │                             │
                       └──────────────┬──────────────┘
                                      ▼
                     ┌────────────────────────────────────────┐
                     │      Scoring & Feedback Engine         │
                     │────────────────────────────────────────│
                     │ • Score Aggregation (0–100 per Judge)  │
                     │ • Strength/Weakness Analysis           │
                     │ • Missing Element Detection            │
                     │ • Recommended Fixes & Improvements     │
                     │ • Optimized Pitch/Demo Flow            │
                     └──────────────────┬─────────────────────┘
                                        │
                                        ▼
                     ┌──────────────────────────────────────────┐
                     │       Frontend Visualization Layer       │
                     │──────────────────────────────────────────│
                     │ • Score Charts (Tech / Impact / UX)      │
                     │ • Detailed Feedback Cards                │
                     │ • Improvement Checklist                  │
                     │ • Final Predicted Judge Score            │
                     └──────────────────────────────────────────┘
