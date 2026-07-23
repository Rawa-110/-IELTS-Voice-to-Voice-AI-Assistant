# -IELTS-Voice-to-Voice-AI-Assistant

# 🎙️ IELTS Voice-to-Voice AI Assistant

## 📌 Project Overview

The IELTS Voice-to-Voice AI Assistant is an intelligent voice assistant designed to simulate the IELTS Speaking Test. The system accepts spoken English from the user, converts it into text using OpenAI Whisper, evaluates the response using Cohere's Large Language Model (LLM), and generates spoken feedback using Google Text-to-Speech (gTTS).

This project demonstrates the integration of Speech-to-Text (STT), Large Language Models (LLMs), and Text-to-Speech (TTS) technologies to create a complete AI-powered voice assistant.

---

## 🚀 Features

- 🎤 Record or upload speech.
- 📝 Convert speech to text using Whisper.
- 🤖 Evaluate responses with Cohere AI.
- 📊 Estimate an IELTS Speaking Band Score.
- 💡 Provide grammar and vocabulary feedback.
- ❓ Ask the next IELTS Speaking question.
- 🔊 Convert AI responses into natural speech.

---

## 🛠 Technologies Used

- Python
- Google Colab
- OpenAI Whisper
- Cohere API
- gTTS (Google Text-to-Speech)
- FFmpeg

---

## 📂 Project Structure

```
IELTS-Voice-Assistant/
│
├── app.ipynb
├── requirements.txt
├── README.md
├── audio/
│   ├── input.mp4
│   └── output.mp3
└── assets/
```

---

## ⚙️ Installation

Install the required Python libraries:

```bash
pip install openai-whisper
pip install cohere
pip install gTTS
pip install soundfile
pip install ffmpeg-python
```

If FFmpeg is not installed:

```bash
sudo apt update
sudo apt install ffmpeg
```

For Google Colab:

```python
!apt-get update
!apt-get install -y ffmpeg
```

---

## ▶️ How to Run

### Step 1
Install all required libraries.

### Step 2
Upload or record an audio file.

### Step 3
Load the Whisper model.

```python
model = whisper.load_model("base")
```

### Step 4
Convert speech to text.

```python
result = model.transcribe("voice.mp4")
```

### Step 5
Send the text to Cohere.

```python
response = co.chat(message=prompt)
```

### Step 6
Convert the AI response into speech.

```python
tts = gTTS(text=response.text, lang="en")
tts.save("reply.mp3")
```

### Step 7
Play the generated audio.

---

## 🔄 Workflow

```
User Speech
      │
      ▼
Speech-to-Text (Whisper)
      │
      ▼
Cohere Large Language Model
      │
      ▼
Feedback + IELTS Evaluation
      │
      ▼
Text-to-Speech (gTTS)
      │
      ▼
Voice Response
```

---

## 📊 Example

### User

> I enjoy reading books because they help me improve my English.

### AI Feedback

```
Grammar: Good

Vocabulary: Good

Fluency: Good

Estimated IELTS Band: 7.0

Suggestion:
Try using more advanced vocabulary and provide more detailed examples.

Next Question:
What do you usually do in your free time?
```

---

## 🎯 Learning Outcomes

- Speech-to-Text using OpenAI Whisper.
- AI text generation with Cohere.
- Text-to-Speech using gTTS.
- Building a complete Voice-to-Voice AI Assistant.
- API integration.
- Audio processing in Python.

---

## 📜 License

This project is created for educational purposes.
