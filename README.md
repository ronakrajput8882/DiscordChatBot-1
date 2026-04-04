<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,12,24&height=200&section=header&text=🤖%20Discord%20ChatBot&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=AI-Powered%20Discord%20Bot%20|%20Python%20+%20OpenAI%20API%20+%20Heroku&descAlignY=60&descAlign=50" width="100%"/>

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Discord.py](https://img.shields.io/badge/discord.py-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discordpy.readthedocs.io)
[![OpenAI](https://img.shields.io/badge/OpenAI%20API-412991?style=for-the-badge&logo=openai&logoColor=white)](https://platform.openai.com)
[![Heroku](https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white)](https://heroku.com)
[![python-dotenv](https://img.shields.io/badge/python--dotenv-ECD53F?style=for-the-badge&logo=python&logoColor=black)](https://pypi.org/project/python-dotenv)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)

</div>

---

## 📌 Project Overview

**DiscordChatBot** is an AI-powered Discord bot built with Python that integrates the **OpenAI API** to respond intelligently to messages in any Discord server. Users can chat with the bot directly in a channel and get GPT-powered replies in real time. The bot is deployed on **Heroku** for 24/7 uptime.

> 🎯 Combines Discord's bot framework with OpenAI's language model — making any Discord server smarter with conversational AI.

---

## 🔄 Bot Workflow

```
User Message in Discord → discord.py Event Listener → OpenAI API Call (httpx) → AI Response → Discord Channel
```

### 1️⃣ Event Listener
- Bot connects to Discord using `discord.py` and listens for `on_message` events
- Filters messages to ignore other bots and only respond to human users
- Triggers on mentions or specific channel messages

### 2️⃣ OpenAI API Integration
- User message is forwarded to the OpenAI Chat Completion endpoint via `httpx`
- GPT model generates a contextual, intelligent response
- Response is returned and sent back into the Discord channel

### 3️⃣ Environment & Deployment
- API keys and tokens stored securely in `.env` using `python-dotenv`
- `Procfile` configures the worker process for Heroku deployment
- Bot runs as a persistent worker — always online, no manual restarts

---

## 🔍 Key Highlights

- 🧠 **OpenAI-powered replies** — every message gets a real GPT response, not hardcoded answers
- 🔐 **Secure config** — Discord token and OpenAI key loaded from `.env`, never hardcoded
- ☁️ **Heroku deployed** — `Procfile` worker keeps the bot running 24/7 in the cloud
- ⚡ **httpx for async HTTP** — non-blocking API calls for fast, responsive bot replies
- 🐍 **Pure Python** — single `main.py` entry point, clean and minimal codebase

---

## 🗂️ Repository Structure

```
DiscordChatBot-1/
│
├── main.py              # Bot logic — event listeners, OpenAI API calls, response handling
├── requirements.txt     # Dependencies: discord.py, httpx, python-dotenv
├── Procfile             # Heroku worker process config
└── README.md
```

---

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Discord Bot Token ([Discord Developer Portal](https://discord.com/developers/applications))
- OpenAI API Key ([platform.openai.com](https://platform.openai.com))
- Heroku account (for cloud deployment)

### 1. Clone the repo
```bash
git clone https://github.com/ronakrajput8882/DiscordChatBot-1.git
cd DiscordChatBot-1
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Create `.env` file
```env
DISCORD_TOKEN=your_discord_bot_token
OPENAI_API_KEY=your_openai_api_key
```

### 4. Run locally
```bash
python main.py
```

### 5. Deploy to Heroku
```bash
heroku login
heroku create your-bot-name
heroku config:set DISCORD_TOKEN=your_token
heroku config:set OPENAI_API_KEY=your_key
git push heroku main
heroku ps:scale worker=1
```

---

## 🧠 Key Learnings

- Integrating OpenAI's Chat Completion API into a real-time event-driven application
- Using `discord.py`'s async event system (`on_message`, `on_ready`) to handle live Discord events
- Making async HTTP calls with `httpx` instead of `requests` for non-blocking bot performance
- Deploying a persistent Python worker to Heroku using a `Procfile` for 24/7 bot uptime
- Securing credentials with `python-dotenv` — a best practice for any API-integrated project

---

## 🛠️ Tech Stack

| Tool | Purpose |
|:---|:---|
| Python 3.10+ | Core language |
| discord.py | Discord bot framework & event handling |
| OpenAI API | GPT-powered chat response generation |
| httpx | Async HTTP client for OpenAI API calls |
| python-dotenv | Secure environment variable management |
| Heroku | Cloud deployment with 24/7 worker uptime |

---

<div align="center">

### Connect with me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ronaksinh-rajput8882)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/techwithronak)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ronakrajput8882)

*If you found this useful, please ⭐ the repo!*

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,12,24&height=100&section=footer" width="100%"/>

</div>