# 🚆 ADY Ticket Monitor

A cross-platform ticket monitoring tool for **Azerbaijan Railways (ADY)**.

The application monitors ticket availability between **Tbilisi** and **Baku** and notifies users immediately when seats become available.

> ⚠️ This project is under active development.

---

## Features

### Current

- Playwright browser automation
- Persistent browser session
- Automatic cookie management
- ADY API client
- macOS notification
- Telegram notification
- Configurable monitoring interval
- Multi-date monitoring
- Logging

### Planned

- Desktop GUI (PySide6)
- macOS `.app`
- Menu bar application
- SQLite history
- Auto update
- Multiple railway providers

---

## Project Structure

```text
app/
├── api/
├── browser/
├── config/
├── monitor/
├── notify/
├── pages/
├── ui/
└── utils/

config/
logs/
screenshots/
tests/
```

---

## Requirements

- Python 3.12+
- Playwright
- Chromium

macOS is currently the primary development platform.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/iMrCuriosity/ADY-Ticket-Monitor.git

cd ADY-Ticket-Monitor
```

Create virtual environment:

```bash
python3 -m venv .venv
```

Activate:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Install Playwright browser:

```bash
playwright install chromium
```

Run:

```bash
python -m app.main
```

---

## Configuration

Configuration will be stored in:

```
config/config.json
```

Example:

```json
{
  "route": {
    "from": "Tbilisi",
    "to": "Baku RWS"
  },
  "dates": [
    "2026-08-15"
  ],
  "interval": 120,
  "headless": true
}
```

---

## Development Roadmap

### v0.1

- Project bootstrap
- Browser automation
- Ticket monitor
- macOS notification

### v0.2

- API client
- SQLite
- Telegram notification

### v0.3

- Desktop GUI
- Menu bar
- Packaging

### v1.0

- macOS App
- Automatic update
- Multi-provider support

---

## Tech Stack

- Python 3.12
- Playwright
- Requests
- PySide6
- Pydantic
- Loguru
- SQLite
- Typer
- PyInstaller

---

## Contributing

Issues and pull requests are welcome.

---

## License

MIT License
