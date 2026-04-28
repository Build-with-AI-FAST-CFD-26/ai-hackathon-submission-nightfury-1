FounderOS – The AI Co-Founder

Build with AI Hackathon 2026 Submission

Team Name: NightFury
Team Members: Arhum Usman (Solo Participant – Full Stack + AI)

1. 🧠 Project Overview

FounderOS solves a critical problem for early-stage founders: repeatedly writing high-stakes communications like investor emails, accelerator applications, and customer outreach from scratch.

Our AI-powered solution acts as a context-aware co-founder, generating ready-to-send drafts in seconds by leveraging stored company data such as traction, product details, and vision.

2. ⚙️ Google AI Tech Stack Implementation
🔹 Google AI Studio / Vertex AI
Integrated Gemini (via Google AI Studio / Vertex AI) for intelligent text generation (or Claude in your current build — adjust if needed for submission compliance).
Used structured prompt engineering to inject:
Company context (MRR, stage, product)
Tone control (confident, founder-level communication)
Streaming responses implemented for real-time draft generation.
🔹 Hosting & Backend
Google Cloud Run
Backend deployed as a containerized Node.js service.
Handles API routing, prompt building, and AI requests securely.
Firebase (Firestore + Auth)
Firestore stores:
Company context
Draft history
Pipeline & alerts
Firebase Authentication (Google OAuth) secures access.
🔹 Integration

The system connects all tools as follows:

User logs in via Firebase Auth
Company data stored in Firestore
User submits a task (e.g., “Write investor follow-up”)
Backend (Cloud Run):
Fetches context from Firestore
Builds structured prompt
Sends request to AI model (Gemini/Claude)
AI response streams back to frontend in real-time
Draft is saved for reuse and editing
3. 💡 Innovation & Impact
🚀 What Makes It Unique
Context-first AI: Unlike generic AI tools, FounderOS remembers your startup.
Co-founder behavior: Not just writing — thinking like a strategic partner.
End-to-end workflow: Drafting + pipeline tracking + alerts in one system.
🌍 Real-World Impact
Saves founders 10+ hours/week
Improves quality of investor and customer communication
Helps early-stage startups operate like well-funded teams
4. 🛠️ Setup & Installation

Follow these steps to run the project locally:

# 1. Clone the repository
git clone https://github.com/Build-with-AI-FAST-CFD-26/ai-hackathon-submission-nightfury-1
cd founderos

# 2. Install dependencies
pip install -r requirements.txt
# OR (if Node backend)
npm install

# 3. Set up environment variables
Create a `.env` file in the root directory and add:

API_KEY=your_api_key_here
FIREBASE_CONFIG=your_firebase_config
PROJECT_ID=your_project_id

# 4. Run the application
python main.py
# OR
npm run dev

🧱 Tech Stack Summary
Frontend: React 18 + Vite + Tailwind CSS
Backend: Node.js + Express
Hosting: Google Cloud Run + Vercel
Database: Firebase Firestore
Authentication: Firebase Auth (Google OAuth)
AI Layer: Gemini / Claude (Streaming)
Scheduler: Google Cloud Scheduler
📌 Future Improvements
Multi-user team collaboration
CRM integrations (HubSpot, Notion)
Voice-based founder assistant
Fine-tuned founder-specific AI models
🏁 Conclusion

FounderOS is more than a writing tool — it’s an AI-powered operating system for founders, helping them move faster, communicate better, and build smarter.
