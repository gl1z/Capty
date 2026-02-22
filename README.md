# Capty

Get the transcript of any YouTube video instantly. Free, no signup, no API keys.

## Stack

- **Frontend** — Vanilla HTML/CSS/JS, Geist font
- **Backend** — Node.js + Express
- No external APIs, no API keys required

## How it works

The backend fetches the YouTube page server-side (bypassing browser CORS restrictions),
extracts the caption track data embedded in the page, then fetches and parses the
caption XML — returning clean plain text to the frontend.

## Run locally

```bash
npm install
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000)

## Deploy

Works on any Node.js host: Railway, Render, Fly.io, or a VPS.
