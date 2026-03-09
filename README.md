# Capty

**[Live Demo →](https://capty-izpe.onrender.com)**

Paste a YouTube URL, get the full transcript. Timestamped segments link back to the exact moment in the video.

Works with any video that has captions. Falls back to OpenAI Whisper for videos without subtitles. Translates into 15 languages.

> **Requires an OpenAI API key** for Whisper transcription and translation. Caption extraction from videos that already have subtitles is free and uses no API credits.

## Setup

Node.js 20+ and Python 3 with `yt-dlp` installed.

```bash
git clone https://github.com/gl1z/capty.git
cd capty
npm install
```

Create a `.env` file in the root:

```
OPENAI_API_KEY=sk-your-key-here
```

```bash
npm start
```

Opens at `http://localhost:3000`.

### Docker

```bash
docker build -t capty .
docker run -p 3000:3000 -e OPENAI_API_KEY=sk-your-key-here capty
```

## Features

- **Timestamped output** - each line shows `[M:SS]` linking to that point in the video
- **Caption extraction** - pulls existing subtitles via yt-dlp, no API cost
- **Whisper fallback** - generates transcript from audio when no captions exist (uses OpenAI API)
- **Translation** - GPT 4o mini translation into 15 languages (uses OpenAI API)
- **Export** - download as `.txt`, `.pdf`, or `.docx`, with optional timestamps included
- **History** - recent videos stored locally in the browser
- **Side-by-side translation** - original and translated transcript shown in parallel columns
- **Video titles in history** - recent panel shows the video title instead of the ID
## Env vars

| Variable | Required | Description |
|----------|----------|-------------|
| `OPENAI_API_KEY` | Yes | From [platform.openai.com](https://platform.openai.com) |
| `PORT` | No | Defaults to 3000 |

## License

MIT

---

Built by [@gl1z](https://github.com/gl1z)

