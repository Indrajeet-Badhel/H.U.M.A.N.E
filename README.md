# H.U.M.A.N.E
### Hyper-Understanding Multi-modal Assistant with Neural Emotions

H.U.M.A.N.E is a multi-modal assistant that combines voice, image, and emotional tone to produce context-aware, emotionally adaptive responses. It handles real-time conversation, safety filtering, and expressive voice output — all wired together through a modular pipeline.

---

## What It Does

- Transcribes and tone-analyzes voice input using Whisper
- Captures, enhances, and classifies images on the fly
- Converts raw input into structured prompts with memory context
- Filters explicit or unsafe content at voice, text, and image levels
- Generates emotionally adjusted text-to-speech responses
- Tracks multi-turn conversation history
- Protects personal info using a context-aware safety layer
- Communicates in real time via WebSocket

---

## Project Structure

```
humane-ai/
│
├── backend/                    # WebSocket server and API handlers
│   ├── web_server.py
│   └── websocket_handler.py
│
├── web/                        # Frontend UI
│   ├── assets/
│   │   ├── css/
│   │   │   ├── app.css
│   │   │   ├── landing.css
│   │   │   └── styles.css
│   │   └── js/
│   │       ├── app.js
│   │       ├── animations.js
│   │       ├── landing.js
│   │       └── voice-controller.js
│   ├── app.html
│   └── index.html
│
├── voice_input/                # Voice capture and Whisper transcription
├── prompt_converter/           # Converts tone, image, and text into prompts
├── safety_guard/               # Content filtering (explicit/harmful input)
├── tts_output/                 # Emotion-based text-to-speech
├── templates/                  # HTML templates (Flask)
├── utils/                      # Helper functions and memory management
├── main.py                     # Entry point — connects all modules
├── agent_manager.py            # Multi-agent pipeline logic
├── .env                        # API keys
└── pipeline_results.json       # Stores latest conversation/memory state
```

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/humane-ai.git
cd humane-ai
```

### 2. Set up a virtual environment

```bash
python -m venv whisper_env
source whisper_env/Scripts/activate   # Windows
# source whisper_env/bin/activate     # macOS/Linux
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

To generate `requirements.txt` from your current environment:

```bash
pip freeze > requirements.txt
```

### 4. Configure environment variables

Add your keys to `.env`:

```
DEEPAI_API_KEY=your_key_here
HF_API_TOKEN=your_key_here
DANDELION_API_TOKEN=your_key_here
COHERE_API_KEY=your_key_here
```

---

## How It Works

```
Voice Input
   → Whisper transcription + tone analysis
   → Image capture, enhancement, and classification (if applicable)
   → Prompt converter (memory personalization, context injection)
   → Safety guard (content filtering)
   → LLM response generation
   → Emotion amplifier
   → Voice output
```

Each stage is modular. The `agent_manager.py` coordinates the pipeline, and `main.py` ties everything together.

---

## Web UI

The frontend lives in `/web/`. Key files:

- `app.html` — main app interface
- `app.js` — core logic
- `voice-controller.js` — handles mic input and voice events
- `animations.js` — UI animations
- `app.css`, `landing.css`, `styles.css` — styling

---

## Privacy and Safety

Explicit content is filtered at every input stage (voice, text, image). The system does not persist personal data unless the user explicitly enables multi-turn memory. Conversations are ephemeral by default.

---

## Roadmap

- [ ] Docker setup and deployment script
- [ ] Local model support (Ollama, HuggingFace local)
- [ ] Real-time webcam input for emotional mirroring
- [ ] Progressive Web App (PWA) version
- [ ] Visual avatar for response feedback

---

## Demo

[Watch the demo on YouTube](https://youtu.be/GAICcOX4VJY)

---

## Credits

Built by **Indrajeet Badhel**  
Vishwakarma Institute of Technology  
Areas of focus: AI, Robotics, Automation
