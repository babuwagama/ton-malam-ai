TON Malam AI – App Architecture

 Overview

TON Malam AI uses a simple AI-first architecture where:
- Frontend handles UI (Next.js)
- AI Tutor handles learning (OpenAI API)
- Data is stored locally or lightweight DB (for MVP)



 Core Data Flow

User → UI (Next.js)
     → API Route (/api/ai-tutor)
     → OpenAI API
     → Hausa Response
     → UI Display



 Modules

 1. AI Tutor Module
- Endpoint: `/api/ai-tutor`
- Input: user question
- Output: Hausa explanation

 2. Lessons Module
- Static JSON or DB
- Structure:
  - id
  - title
  - content (Hausa)
  - level

 3. Quiz Module
- Questions stored in JSON
- Score tracked in localStorage

 4. Progress Module
- Tracks:
  - completed lessons
  - quiz scores
- Stored in localStorage (MVP)



 Security (MVP Level)
- No sensitive data stored
- Wallet connection optional (TON Connect later stage)



 Deployment
- Frontend: Vercel
- API: Vercel serverless functions
