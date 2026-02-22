# Capty

Get the transcript of any YouTube video instantly. Free, no signup, no BS.

**[Live Demo →](https://capty.onrender.com)** *(https://capty-izpe.onrender.com)*

![screenshot](https://github.com/user-attachments/assets/placeholder)

## Features

- Paste any YouTube URL → get the transcript
- Multiple languages (English, Spanish, German, Japanese, Chinese, Russian)
- Copy to clipboard
- Download as .txt, .pdf, or .doc
- Clean, minimal dark UI
- No API keys required

## Run Locally

**Requirements:** [Node.js](https://nodejs.org/) + [Python 3](https://python.org/) + [yt-dlp](https://github.com/yt-dlp/yt-dlp)

```bash
# 1. Clone the repo
git clone https://github.com/gl1z/capty.git
cd capty

# 2. Install dependencies
npm install
pip install yt-dlp

# 3. Start the server
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000)

## Deploy with Docker

```bash
docker build -t capty .
docker run -p 3000:3000 capty
```

Or deploy to [Render](https://render.com), [Railway](https://railway.app), or any platform that supports Docker.

## How It Works

1. User pastes a YouTube URL
2. Backend uses `yt-dlp` to fetch available subtitle tracks
3. User selects a language
4. Backend downloads the subtitle file and parses it to plain text
5. Frontend displays the transcript with copy/download options

## Stack

- **Frontend** — Vanilla HTML/CSS/JS, Geist + Noto Sans fonts
- **Backend** — Node.js, Express
- **Subtitles** — [yt-dlp](https://github.com/yt-dlp/yt-dlp)

## License

MIT

---

Built by [@gl1z](https://github.com/gl1z)
