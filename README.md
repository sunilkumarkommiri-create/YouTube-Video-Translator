# 🎥 YouTube Video Translator (AI)

An AI-powered project that translates YouTube videos into multiple languages using speech recognition and text-to-speech.

---

## 🚀 Features

* 🎧 Extracts audio from YouTube videos
* 🧠 Converts speech to text using AI
* 🌍 Translates text into different languages
* 🔊 Generates translated audio output
* ⚡ Works in Google Colab (no setup required)

---

## 🛠️ Technologies Used

* Python
* yt-dlp (YouTube downloader)
* OpenAI Whisper (Speech-to-Text)
* Deep Translator (Translation)
* gTTS (Text-to-Speech)

---

## 📌 How It Works

1. Input a YouTube video URL
2. Download the audio from the video
3. Convert speech → text using Whisper
4. Translate text into target language
5. Convert translated text → speech
6. Download translated audio

---

## ▶️ How to Run (Google Colab)

1. Open Google Colab
2. Install dependencies:

```
!pip install yt-dlp openai-whisper deep-translator gtts
!apt-get update -y
!apt-get install -y ffmpeg
```

3. Restart runtime

4. Run the main script

---

## 💻 Example Code

```python
import yt_dlp
import whisper
from deep_translator import GoogleTranslator
from gtts import gTTS
import os

url = "YOUR_YOUTUBE_LINK"

ydl_opts = {
    'format': 'bestaudio',
    'outtmpl': 'audio.%(ext)s',
    'noplaylist': True,
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download(
```
