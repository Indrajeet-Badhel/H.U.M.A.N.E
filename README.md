# 🧠 H.U.M.A.N.E - Hyper-Understanding Multi-modal Assistant with Neural Emotions

H.U.M.A.N.E is an intelligent, multi-modal assistant that combines voice, image, and emotional tone to deliver human-like, emotionally adaptive responses. The system is designed for secure, context-aware conversations and interactive AI behaviors.

---

## 🌟 Features

- 🎙️ Voice Input & Sentiment Analysis  
- 🧠 AI-Driven Prompt Conversion & Memory Handling  
- 📸 Image Capture, Enhancement & Classification  
- 🧾 Safety Guardrails for Explicit/Unsafe Inputs  
- 🗣️ Emotion-Amplified Text-to-Speech Generation  
- 🔄 Multi-Turn Conversation Memory  
- 🕵️ Personal Info Guard & Context Tracker  
- ⚡ WebSocket-Driven Real-Time Communication  

---

## 🗂️ Project Structure

```bash
humane-ai/
│
├── backend/ # Python backend logic (WebSocket, APIs)
│ ├── web_server.py
│ └── websocket_handler.py
│
├── web/ # Web UI
│ ├── assets/
│ │ ├── css/
│ │ │ ├── app.css
│ │ │ ├── landing.css
│ │ │ └── styles.css
│ │ └── js/
│ │ ├── app.js
│ │ ├── animations.js
│ │ ├── landing.js
│ │ └── voice-controller.js
│ ├── app.html
│ └── index.html
│
├── voice_input/ # Voice capture & Whisper-based transcription
├── prompt_converter/ # Converts tone/image/text into structured prompts
├── safety_guard/ # Filters for explicit content and harmful data
├── tts_output/ # Emotion-based text-to-speech generation
├── templates/ # Optional HTML templates (if using Flask)
├── utils/ # Helper functions & memory management
├── main.py # Entry point (connects all agents)
├── agent_manager.py # Handles multi-agent pipeline logic
├── .env # API keys (Whisper, HuggingFace, Cohere, etc.)
└── pipeline_results.json # Stores latest conversation/memory info

```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/humane-ai.git
cd humane-ai
```
2. Create & Activate Virtual Environment
```bash
python -m venv whisper_env
source whisper_env/Scripts/activate  # On Windows
```
3. Install Dependencies
```bash
pip install -r requirements.txt
```
You can generate requirements.txt with:
```bash
Copy code
pip freeze > requirements.txt
```
4. Set Environment Variables
Update .env with the following:
```bash
DEEPAI_API_KEY=your_key_here
HF_API_TOKEN=your_key_here
DANDELION_API_TOKEN=your_key_here
COHERE_API_KEY=your_key_here
```

## Functional Flow
css
```bash

[User Voice] --> [Whisper + Tone Analyzer] --> [Prompt + Image Handler] -->
[Memory Layer + Safety Guard] --> [LLM Agent(s)] --> [TTS Output (emotional)] --> [Voice Reply]
```
Voice Input is transcribed and tone-analyzed

Images (if any) are captured, enhanced, classified

Prompt converter ensures memory personalization and AI tuning

AI modules generate response, updated via conversation memory

Emotion Amplifier adjusts the voice response tone

## Web UI Interaction
HTML: /web/app.html

JS Controllers: app.js, voice-controller.js, animations.js

Styling: app.css, landing.css, styles.css

## Security & Ethics
⚠️ Explicit content is filtered at voice, text, and image levels

🧠 AI does not store or share personal data without safety validation

⏱️ Conversations are ephemeral unless user allows multi-turn memory
## Future Roadmap

 Docker + deployment script

 GPT-Free model switch (Ollama, LocalHF)

 Real-time webcam integration for emotional mirroring

 Progressive Web App (PWA) version

 GUI/Avatar for visual feedback

### Credits
Created by Indrajeet Badhel
🎓 Vishwakarma Institute of Technology
💡 Focused on AI, Robotics, Blockchain

