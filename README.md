# Keyboard Master

A typing practice web app built with Python (PySide6) and ported to a single-file HTML/JavaScript web app. Practice your typing speed and accuracy with real-time feedback, error tracking, and WPM calculation.

## Features

- **Three difficulty tiers** — Easy (1 sentence), Medium (2 sentences), Hard (3-4 sentences)
- **Real-time character highlighting**
  - 🟢 Green — correct
  - 🔴 Red — incorrect
  - 🟡 Amber — corrected (was wrong, now fixed)
  - Gray — not yet typed
- **Persistent error tracking** — characters that were ever mistyped stay amber even after correction
- **Live WPM counter** — updates every second while typing
- **Completion screen** — shows time, WPM, errors, corrections, and accuracy percentage
- **Dark/Light mode toggle**
- **Keystroke sound** — generated via Web Audio API, no external files needed
- **Auto word-wrap** — text wraps cleanly at word boundaries, no mid-word splits
- **Auto scroll** — follows your current typing position

## Demo

Visit the live site at: `https://simjedo.github.io/keyboard-master`

## Usage

Just open `index.html` in any modern browser — no installation or dependencies required.

1. Select a difficulty from the dropdown
2. Click **Start New Practice**
3. Type the displayed text as fast and accurately as you can
4. View your results when done
5. Click **Start New Practice** to try again

## Project Structure

```
keyboard-master/
├── index.html        # entire app — HTML, CSS, and JS in one file
└── README.md
```

## Desktop Version

The original desktop version is built with Python and PySide6 and includes:
- Native keyboard click WAV sound effect
- Same highlighting and scoring logic

### Requirements

```
PySide6
PySide6-Addons
```

### Run locally

```bash
pip install PySide6 PySide6-Addons
python main.py
```

## Scoring

| Metric | Description |
|--------|-------------|
| WPM | Characters typed divided by 5, divided by minutes elapsed |
| Errors | Characters still wrong at completion |
| Corrections | Characters that were wrong at some point but fixed |
| Accuracy | Percentage of characters never mistyped |

## License

MIT
