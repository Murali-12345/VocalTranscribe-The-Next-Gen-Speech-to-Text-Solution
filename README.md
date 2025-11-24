# VocalTranscribe: The Next-Gen Speech-to-Text Solution

**VocalTranscribe** is an advanced Speech-to-Text system combining deep learning, robust audio processing, and NLP-based refinement to deliver highly accurate transcriptions and a seamless voice-driven assistant experience.

---

##  Features  
- High-accuracy speech recognition with deep-learning models  
- Robust audio preprocessing (noise reduction, voice-activity detection)  
- English-only support (for this version)  
- Chatbot/assistant capabilities via an LLM integration  
- Streaming and batch STT support  
- Example modules for TTS output

---

##  System Architecture  
> **Note:** This version supports **English-only transcription**.

The architecture consists of:  
1. **Audio acquisition & preprocessing** – cleaning audio, detecting speech segments  
2. **Deep learning STT module** – converts audio to raw text output  
3. **LLM/NLP post-processor** – refines the raw text, adds context & formatting  
4. **TTS / output module** – (optional) converts refined text back to speech  
5. **Agent controller** – Manages workflow: audio → transcription → refinement → output (or chat)

---

##  Project Structure  
VocalTranscribe/
├── QuickAgent.py               # Main agent/controller script
├── README.md                   # Project documentation
├── llm.py                      # LLM integration & utilities
├── output.wav                  # Sample output audio
├── requirements.txt            # Python library dependencies
├── speech_to_text_streaming.py # Streaming STT implementation
├── system_prompt.txt           # System instructions for the LLM
├── text_to_speech.py           # TTS module


---

## ⚙️ Installation  
```bash
git clone https://github.com/Murali-12345/VocalTranscribe-The-Next-Gen-Speech-to-Text-Solution.git
cd VocalTranscribe-The-Next-Gen-Speech-to-Text-Solution
pip install -r requirements.txt

```

---

## Usage
1. Run the Full Agent (STT → LLM → TTS)

This runs the entire pipeline:
🎤 Speak → Transcription →  LLM Response →  TTS Output
```bash
python QuickAgent.py
```

2. Offline / File-based Speech-to-Text
```bash
python speech_to_text_streaming.py --input audio.wav
```

Example:
```bash
python speech_to_text_streaming.py --input samples/english_test.wav
```

3. Use the STT Module Inside Your Own Code

```python
from speech_to_text_streaming import SpeechToText

stt = SpeechToText()
result = stt.transcribe_audio("audio.wav")
print(result)
```

4. Text-to-Speech Conversion














