# SixFold: Cognitive Gaming and Memory Assistance Platform

**Smart India Hackathon 2026** | Problem Statement ID: **SIH26003** | Category: **Software**

> AI-Based Cognitive Gaming and Memory Assistance Platform for Elderly Dementia Patients in North Eastern Region (NER)

A culturally aware, multilingual and AI-assisted cognitive gaming platform that adapts to each elderly user's performance, while giving caregivers meaningful visibility into engagement and progress.

> **Note:** This platform supports cognitive engagement and assists memory activities. It is **not** a diagnostic tool and **not** a replacement for doctors or medical care.

---

## Overview

Elderly users, including dementia patients, play simple cognitive games with content drawn from North Eastern Indian contexts. The platform learns from how each user performs and personalizes the experience, while a caregiver dashboard shows activity and progress over time.

## Key Features

- **Cognitive games** with three core game types
- **AI-based personalization** of difficulty, content and recommendations
- **Game-specific adaptive difficulty** instead of one universal score
- **NER-specific content**: local food, crafts, clothing, architecture, flora and fauna, landscapes and markets
- **Multilingual support** with user-selectable language
- **Voice-assisted interaction** (speech-to-text and text-to-speech)
- **Elderly-friendly UI**: large buttons, high contrast, simple layouts, low cognitive load
- **Caregiver dashboard** with performance analytics, progress trends and AI insights

## Games

| Game | What it tests |
|------|---------------|
| **Memory Match** | Memory and recognition |
| **Remember the Scene** | Visual memory and attention |
| **Sequence Recall** | Working memory and sequencing |

The architecture is designed so more games can be added later.

## System Architecture

```
Elderly User (Text / Voice / Touch)
        |
   React + Vite Frontend
        |
   Node.js + Express Backend  (JWT-protected APIs)
        |
   +----+-----------------+------------------+
   |                      |                  |
Game Engine     AI Personalization     Language Layer
   |                      |                  |
   +----------------------+------------------+
        |
   PostgreSQL Database
        |
   Caregiver Dashboard (Analytics + Insights)
```

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React, Vite, HTML/CSS/JavaScript |
| Backend | Node.js, Express.js |
| Database | PostgreSQL (`pg`) |
| Authentication | JWT |
| Intelligent layer | Adaptive personalization engine, NLP / language processing, speech-to-text and text-to-speech |

## Project Structure

```
sixfold-sih2026/
├── frontend/    # React + Vite app
├── backend/     # Node.js + Express API
├── database/    # SQL schema and migrations
├── docs/        # Presentation, diagrams and notes
└── README.md
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) (LTS)
- [Git](https://git-scm.com)
- [PostgreSQL](https://www.postgresql.org) (when working on the database)

### Setup

```bash
git clone https://github.com/s-zarar44/sixfold-sih2026.git
cd sixfold-sih2026

# Frontend
cd frontend
npm install
npm run dev        # runs on http://localhost:5173

# Backend (in a new terminal)
cd backend
npm install
node index.js      # runs on http://localhost:5000
```

### Environment variables

Create a `.env` file inside `backend/` for local secrets such as the database URL and JWT secret. **Never commit `.env` files.**

## Team Workflow

1. Never push directly to `main`.
2. Get the latest code: `git checkout main` then `git pull origin main`.
3. Create a branch for your task: `git checkout -b feature/short-task-name`.
4. Commit small and often, with clear messages.
5. Push your branch and open a **Pull Request** into `main`.
6. A teammate reviews and approves before it is merged.

## Team SixFold

| Name | Role / Area |
|------|-------------|
| _Member 1_ | _e.g. Frontend and games_ |
| _Member 2_ | _e.g. Frontend and games_ |
| _Member 3_ | _e.g. Backend and database_ |
| _Member 4_ | _e.g. Backend and database_ |
| _Member 5_ | _e.g. AI and personalization_ |
| _Member 6_ | _e.g. Multilingual, voice and content_ |

## License

To be decided by the team.