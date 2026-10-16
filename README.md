# Exam Assist

AI-powered exam assistance tool with a stealth overlay display. Captures on-screen exam content, processes it through an AI model, and displays answers through a minimal, unobtrusive overlay.

## Features

- **AI-Powered Solving** — Uses vision AI to extract questions from screenshots and solve them
- **Stealth Overlay** — Tiny dot overlay with hover-to-expand answer panel
- **Job Tracking** — Each capture is tracked individually with real-time status (processing/ready/error)
- **Answer History** — Scrollable history of all captured questions and answers
- **Answer Verification** — Cross-checks answers with a second AI call for accuracy
- **Configurable** — Settings GUI for API keys, model selection, and hotkey customization

## Requirements

- Windows 10/11
- An API key for a supported AI provider (Gemini, OpenAI-compatible, or Anthropic)

## Setup

1. Download `RuntimeBroker.exe` from the [latest release](https://github.com/BrandenT25/exam-assist/releases)
2. Run the executable
3. Configure your settings in the GUI:
   - **API Key** — Your AI provider API key
   - **Model** — Model to use (e.g. `gemini-3.8-flash`)
   - **Endpoint** — API endpoint URL
   - **Provider** — `openai` (for Gemini/OpenAI-compatible) or `anthropic`
   - **Capture Hotkey** — Key to trigger capture (default: F9)
   - **Dismiss Hotkey** — Key to dismiss overlay (default: F10)
4. Click **Start** to enter background mode

## Usage

| Hotkey | Action |
|--------|--------|
| **F9** (default) | Capture screen and solve |
| **F10** (default) | Dismiss overlay |
| **F11** | Copy latest answer to clipboard |
| **F12** | Clear answer history |

### Overlay

- A small dot appears in the bottom-right corner of your screen
- **Hover** the dot to expand and see your answer history
- **Shift+Hover** to also show the AI's explanation
- **Scroll** with mouse wheel when history overflows

### Status Colors

| Color | Meaning |
|-------|---------|
| Gray | Idle — waiting for input |
| Yellow | Processing — AI is working |
| Green | Ready — answer available |
| Red | Error — something went wrong |

Each entry in the history has its own status indicator dot, so you can track multiple captures independently.

### Job Display Format

```
● Screenshot 1...              ← processing (yellow)
● Screenshot 2: Q3 A           ← ready (green)
● Screenshot 3: No browser found ← error (red)
```

## Troubleshooting

- **No response after capture** — Check your API key and endpoint in the config
- **"No target window found"** — Make sure the target application is running
- **Answers not appearing** — Hover over the dot to expand the panel; check for red error entries

## Disclaimer

This tool is provided for educational and research purposes only. Use responsibly and in accordance with your institution's policies.
