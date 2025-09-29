# 🎙️ AI Voice Agent Engineer – Interview Exercise

Welcome!  
This exercise is designed to test your **real-time coding ability**, **systems thinking**, and how you collaborate while building an **AI voice agent**.  
We’ll start small and extend together as we go. Don’t worry about perfection—focus on clarity, iteration, and communication.

---

## 🥅 Goal
Build a **local voice agent** using [LiveKit Agents (Python)](https://github.com/livekit/agents).  
The agent should:
- Listen to microphone input.
- Transcribe speech into text (with VAD/turn detection).
- Decide how to respond (using a realtime LLM).
- Speak back to the user (TTS).
- Support **barge-in** (stop talking if the user interrupts).
- Keep **short-term memory** (e.g., user’s name).
- Provide **at least one tool** (like telling the current time or setting a timer).

---

## ⚙️ Setup

### 1. Install dependencies
```bash
# Create and activate virtual environment
python -m venv .venv && source .venv/bin/activate

# Install LiveKit agents and plugins
pip install "livekit-agents[openai,silero,turn-detector]~=1.2" \
            "livekit-plugins-noise-cancellation~=0.2" python-dotenv
