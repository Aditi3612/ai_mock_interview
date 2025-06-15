#  Prepwise

**Prepwise** is an AI-powered job interview preparation platform with real-time voice-based interactions. Users can practice interviews using AI voice agents, receive structured feedback via LLMs, and track progress through a dashboard.

---

## 📌 Project Overview

Prepwise enables users to:

- Practice interviews with real-time AI voice agents
- Generate interview questions dynamically based on job role and tech stack
- Get structured feedback scored across categories like communication, technical knowledge, and clarity
- View and manage all past interviews via a personalized dashboard

---

## 🧭 Workflow

1. **User Authentication**  
   Email/password authentication using Firebase Auth.

2. **Interview Initialization**  
   Users select role, level, and tech stack. Questions are generated via a Gemini LLM prompt.

3. **Voice Interview**  
   Vapi AI delivers questions via voice. Responses are transcribed and stored.

4. **Feedback Generation**  
   Transcripts are analyzed using Gemini to return structured scores, strengths, and improvement suggestions.

5. **Dashboard & Review**  
   Users access past sessions, feedback, and transcripts through a personal dashboard.

---

## ⚙️ Tech Stack

- **Frontend:** Next.js, Tailwind CSS, ShadCN/UI  
- **Backend & Auth:** Firebase (Auth, Firestore, Storage)  
- **Voice AI:** Vapi AI (real-time voice interaction)  
- **LLM:** Google Gemini (prompt-based Q&A + scoring)  
- **Validation:** Zod  
- **Deployment:** Vercel (optional)

---

##  Key Features

- Real-time mock interviews via voice
- LLM-based question generation and feedback
- Session-based scoreboards and transcripts
- Responsive UI/UX built with modern web stack
- Firebase-backed authentication and storage
- Modular, reusable code architecture

---
##  Getting Started

### Prerequisites

- Node.js
- Git
- Firebase project
- Vapi account

### Setup Instructions

```bash
git clone https://github.com/yourusername/prepwise.git
cd prepwise
npm install
```

### Environment Variables

Create a `.env.local` file in the root directory and add the following:

```env
NEXT_PUBLIC_VAPI_WEB_TOKEN=
NEXT_PUBLIC_VAPI_WORKFLOW_ID=
GOOGLE_GENERATIVE_AI_API_KEY=
NEXT_PUBLIC_BASE_URL=

NEXT_PUBLIC_FIREBASE_API_KEY=
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=
NEXT_PUBLIC_FIREBASE_PROJECT_ID=
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=
NEXT_PUBLIC_FIREBASE_APP_ID=

FIREBASE_PROJECT_ID=
FIREBASE_CLIENT_EMAIL=
FIREBASE_PRIVATE_KEY=
```

> Replace the placeholder values with your actual credentials from [Firebase](https://firebase.google.com/), [Vapi](https://vapi.ai), and [Google AI Studio](https://makersuite.google.com/).

### Start the Development Server

```bash
npm run dev
```

Then open your browser at:

```
http://localhost:3000
```

---

## 🗂️ Project Structure

```
prepwise/
├── app/                  # Routing and pages (Next.js App Router)
├── components/           # Reusable UI components
├── constants/            # Role and stack mappings
├── firebase/             # Firebase configuration and init
├── lib/                  # Prompt generation, feedback logic, utils
├── public/               # Static assets and icons
├── types/                # TypeScript models and interfaces
└── .env.local            # Environment variables (ignored by Git)
```

