# Entrance Exam Trainer

A web-based entrance exam practice application with verbal, numerical, and abstract reasoning questions.

## Features

- 120 randomized practice questions (40 verbal, 40 numerical, 40 abstract)
- 60-minute timer
- Progress tracking
- Question navigator
- Mark for review functionality
- Detailed results with category breakdown
- Answer review mode

## Local Development

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
python app.py
```

3. Open http://localhost:5000 in your browser

## Deploy to Vercel

### Prerequisites
- Vercel account (sign up at https://vercel.com)
- Git repository with your code

### Deployment Steps

1. **Install Vercel CLI**
```bash
npm install -g vercel
```

2. **Login to Vercel**
```bash
vercel login
```

3. **Deploy**
```bash
vercel
```

Follow the prompts:
- Set up and deploy? → Yes
- Which scope? → Select your account
- Link to existing project? → No
- What's your project's name? → exam-app (or your preferred name)
- In which directory is your code located? → ./
- Want to override the settings? → No

4. **Deploy to production**
```bash
vercel --prod
```

### Alternative: Deploy via Vercel Dashboard

1. Push your code to GitHub
2. Go to https://vercel.com/dashboard
3. Click "Add New Project"
4. Import your GitHub repository
5. Vercel will auto-detect the Python configuration
6. Click "Deploy"

### Important Notes for Vercel Deployment

- The app is configured with `vercel.json` for proper routing
- API routes are handled through `api/index.py`
- Static files (HTML) are served through the Flask app
- The deployment may take a few minutes on first deploy due to Python runtime setup

## Project Structure

```
exam-app/
├── app.py              # Flask application
├── index.html          # Frontend HTML
├── requirements.txt    # Python dependencies
├── vercel.json        # Vercel configuration
├── api/
│   └── index.py       # Vercel serverless function handler
└── README.md          # This file
```
