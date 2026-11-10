# 🎙️ AI Voice Assistant

A streaming AI chat assistant with optional text-to-speech, powered by Google Gemini and built with Gradio.

![Python](https://img.shields.io/badge/Python-3.12+-blue)
![Gradio](https://img.shields.io/badge/Gradio-6.31+-orange)

## Features

- **Streaming Chat** — Real-time token-by-token responses
- **Multiple Models** — Switch between Gemini 3.5 Flash, Gemini 2.5 Flash, and Gemma 4 31B
- **Voice Output** — Optional text-to-speech using Gemini 3.1 Flash TTS
- **Clean UI** — Responsive web interface with Gradio's Ocean theme

## Prerequisites

- **Python 3.12+**
- **[uv](https://docs.astral.sh/uv/)** (recommended) or pip
- **Google API Key** — Get one from [Google AI Studio](https://aistudio.google.com/apikey)

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/ai-voice-assistant.git
cd ai-voice-assistant
```

### 2. Set your API key

```bash
export GOOGLE_API_KEY="your-google-api-key-here"
```

> [!TIP]
> Add the export line to your `~/.zshrc` or `~/.bashrc` to persist it across sessions:
> ```bash
> echo 'export GOOGLE_API_KEY="your-google-api-key-here"' >> ~/.zshrc
> source ~/.zshrc
> ```

### 3. Install dependencies

**Using uv (recommended):**

```bash
uv sync
```

**Using pip:**

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e .
```

## Usage

**Using uv:**

```bash
uv run python main.py
```

**Using pip/venv:**

```bash
source .venv/bin/activate
python main.py
```

The app will launch and open automatically in your browser at `http://127.0.0.1:7860`.

## How It Works

1. **Chat** — Type a message and hit Send (or press Enter). Responses stream in real-time via the OpenAI-compatible Gemini API.
2. **Voice** — Toggle the "Enable voice" checkbox to hear responses spoken aloud using Gemini TTS.
3. **Model Selection** — Pick a model from the dropdown at the top.

## Project Structure

```
ai-voice-assistant/
├── main.py            # Application entry point
├── pyproject.toml     # Project metadata & dependencies
├── uv.lock            # Locked dependency versions
└── README.md
```

## Dependencies

| Package | Purpose |
|---------|---------|
| `openai` | OpenAI-compatible client for Gemini chat API |
| `google-genai` | Google GenAI SDK for text-to-speech |
| `gradio` | Web UI framework |
| `protobuf` | Required by Google GenAI |

## License

This project is open source. Feel free to use and modify it.
