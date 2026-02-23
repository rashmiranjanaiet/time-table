<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# My Performance Hub (Full Stack Local Setup)

This project now runs with:
- Frontend: Vite + React (`http://localhost:3000`)
- Backend: Express API for Gemini (`http://localhost:8787`)

## Prerequisites
- Node.js 18+
- Gemini API key

## 1) Install dependencies

```bash
npm install
```

## 2) Configure backend environment

Create `backend/.env` from `backend/.env.example` and set your key:

```env
GEMINI_API_KEY=your_gemini_api_key_here
PORT=8787
CLIENT_ORIGIN=http://localhost:3000
JWT_SECRET=replace_with_a_long_random_secret
```

## 3) Run frontend + backend together

```bash
npm run dev
```

## Local URLs
- App: `http://localhost:3000`
- API health: `http://localhost:8787/api/health`

## Login and data persistence
- Register or login from the app screen.
- Your tasks and stats are saved per user in `backend/data/db.json`.
- When you login again with the same account, your past data loads automatically.

## Optional frontend env
By default the frontend uses Vite proxy (`/api -> http://localhost:8787`).
If you need a direct API base URL, create `.env.local` with:

```env
VITE_API_BASE_URL=http://localhost:8787
```

## Deploy both frontend + backend on Render
Create 2 services from the same GitHub repo.

1. Backend service (Render `Web Service`)
- Root Directory: repo root
- Build Command: `npm install`
- Start Command: `node backend/server.js`
- Environment Variables:

```env
GEMINI_API_KEY=your_real_key
JWT_SECRET=generate_a_long_random_secret
CLIENT_ORIGIN=https://your-frontend-name.onrender.com
```

2. Frontend service (Render `Static Site`)
- Root Directory: repo root
- Build Command: `npm install && npm run build`
- Publish Directory: `dist`
- Environment Variables:

```env
VITE_API_BASE_URL=https://your-backend-name.onrender.com
```

3. CORS note
- If you use multiple frontend domains, backend `CLIENT_ORIGIN` can be comma-separated:
  `https://your-frontend.onrender.com,https://your-custom-domain.com`
