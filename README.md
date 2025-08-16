# AI Project Idea Generator

An AI-powered web application that generates personalized coding project ideas for developers by analyzing their tech stack, GitHub activity, and resume.

## 🚀 Features

- **GitHub OAuth Integration**: Analyze user's repositories, languages, and coding patterns
- **Resume Analysis**: Parse PDF resumes to extract skills and experience
- **AI-Powered Ideas**: Generate personalized project ideas using GPT-4
- **Feedback System**: Rate and save project ideas to improve recommendations
- **Modern UI**: Built with Next.js and Tailwind CSS
- **Analytics**: Track user interactions with PostHog

## 🏗️ Architecture

```
Idea_gen/
├── frontend/                 # Next.js frontend application
│   ├── components/          # Reusable UI components
│   ├── pages/              # Next.js pages
│   ├── lib/                # Utility functions and API calls
│   └── styles/             # Tailwind CSS styles
├── backend/                 # FastAPI backend application
│   ├── app/                # Main application code
│   │   ├── api/            # API routes
│   │   ├── core/           # Core configuration
│   │   ├── models/         # Database models
│   │   ├── services/       # Business logic
│   │   └── utils/          # Utility functions
│   └── requirements.txt    # Python dependencies
├── .env.example            # Environment variables template
└── README.md              # This file
```

## 🛠️ Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **Tailwind CSS** - Utility-first CSS framework
- **Supabase** - Authentication and real-time database
- **PostHog** - Analytics and user tracking

### Backend
- **FastAPI** - Modern Python web framework
- **OpenAI GPT-4** - AI-powered idea generation
- **GitHub API** - Repository and user data analysis
- **PyMuPDF** - PDF resume parsing
- **Supabase** - Database and authentication

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and npm
- Python 3.9+
- GitHub OAuth App
- OpenAI API key
- Supabase project
- PostHog account

### 1. Clone and Setup

```bash
git clone <your-repo-url>
cd Idea_gen
```

### 2. Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Frontend Setup

```bash
cd frontend
npm install
```

### 4. Environment Variables

Copy `.env.example` to `.env` and fill in your API keys:

```bash
cp .env.example .env
```

### 5. Run Development Servers

**Backend:**
```bash
cd backend
uvicorn app.main:app --reload --port 8000
```

**Frontend:**
```bash
cd frontend
npm run dev
```

Visit `http://localhost:3000` to see the application!

## 📋 API Endpoints

### Authentication
- `POST /auth/github` - GitHub OAuth callback
- `POST /auth/logout` - Logout user

### Resume Analysis
- `POST /resume/upload` - Upload and parse PDF resume

### Project Ideas
- `GET /ideas` - Get AI-generated project ideas
- `POST /ideas/feedback` - Submit feedback on ideas
- `GET /ideas/saved` - Get user's saved ideas

### User Profile
- `GET /profile` - Get user profile and tech stack
- `PUT /profile` - Update user preferences

## 🗄️ Database Schema

### Users Table
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  github_id VARCHAR UNIQUE,
  email VARCHAR,
  name VARCHAR,
  avatar_url VARCHAR,
  tech_stack JSONB,
  skill_level VARCHAR,
  created_at TIMESTAMP DEFAULT NOW()
);
```

### Project Ideas Table
```sql
CREATE TABLE project_ideas (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id),
  title VARCHAR NOT NULL,
  description TEXT,
  match_reason TEXT,
  features JSONB,
  stretch_goals JSONB,
  difficulty VARCHAR,
  created_at TIMESTAMP DEFAULT NOW()
);
```

### Feedback Table
```sql
CREATE TABLE feedback (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id),
  idea_id UUID REFERENCES project_ideas(id),
  rating INTEGER CHECK (rating >= 1 AND rating <= 5),
  feedback_type VARCHAR,
  created_at TIMESTAMP DEFAULT NOW()
);
```

## 🚀 Deployment

### Frontend (Vercel)
1. Connect your GitHub repo to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy automatically on push to main branch

### Backend (Railway/Render)
1. Connect your GitHub repo
2. Set environment variables
3. Deploy with Python runtime

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

MIT License - see LICENSE file for details 

