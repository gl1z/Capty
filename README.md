# Capty

**[Live Demo →](https://capty.onrender.com)** *(https://capty-izpe.onrender.com)*

![screenshot](https://github.com/user-attachments/assets/placeholder)

Paste a YouTube link, get the transcript. That's it.

Works with any video that has captions. If there are no captions, it can transcribe the audio using OpenAI Whisper. You can also translate the result into other languages.

## Setup

You need Node.js 20+, Python 3 with yt-dlp installed, and an OpenAI API key.

```bash
git clone https://github.com/gl1z/capty.git
cd capty
npm install
```

Create a `.env` file in the root:

```
OPENAI_API_KEY=sk-your-key-here
```

Then run it:

```bash
npm start
```

Goes to `http://localhost:3000`.

### Docker

```bash
docker build -t capty .
docker run -p 3000:3000 -e OPENAI_API_KEY=sk-your-key-here capty
```

## What it does

Pulls existing captions from YouTube via yt-dlp. Falls back to Whisper if the video has no subtitles. Translates transcripts using GPT-4o-mini. Lets you copy or download as .txt, .pdf, or .docx.

## Env vars

`OPENAI_API_KEY` — required, get one from platform.openai.com

`PORT` — optional, defaults to 3000

## License

MIT---

Built by [@gl1z](https://github.com/gl1z)

