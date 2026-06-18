# Halcyon Vogue 🌊🎀

A fashion & art blog platform. No followers, no likes — just pure creative expression.

---

## 🚀 Deployment Guide

### BACKEND → Render

1. Create a free account at https://render.com
2. Click **New → Web Service**
3. Upload or connect your GitHub repo with the `halcyon-backend` folder
4. Set these settings:
   - **Build Command:** `npm install`
   - **Start Command:** `node server.js`
5. Add these Environment Variables in Render dashboard:
   - `SESSION_SECRET` → any random string e.g. `halcyon2025supersecret`
   - `FRONTEND_URL` → your Vercel URL (add after deploying frontend)
6. Click **Deploy** — Render gives you a URL like `https://halcyon-vogue-api.onrender.com`

---

### FRONTEND → Vercel

1. Create a free account at https://vercel.com
2. Click **Add New → Project**
3. Upload or connect your GitHub repo with the `halcyon-frontend` folder
4. **Before deploying**, open `config.js` and replace:
   ```
   const API_BASE = 'https://your-backend.onrender.com';
   ```
   with your actual Render URL from above step.
5. Click **Deploy** — Vercel gives you a URL like `https://halcyon-vogue.vercel.app`
6. Go back to Render → Environment Variables → update `FRONTEND_URL` with your Vercel URL
7. Redeploy backend on Render

---

## ✅ Features
- User registration & login
- Upload digi-pics to the feed
- Write & publish blogs
- Create lookbooks (multi-image)
- Create moodboards
- Aesthetic tag filtering
- Beach video hero
- Scrapbook-style lookbook viewer

---

## 📁 Project Structure
```
halcyon-backend/
  server.js        ← Express API
  package.json
  .env.example     ← Copy to .env for local dev
  public/uploads/  ← Uploaded images stored here

halcyon-frontend/
  index.html       ← Full website
  config.js        ← ⚠️ Set your Render URL here
  beach.mp4        ← Hero background video
  vercel.json      ← Vercel routing config
```
