🌐 **[Português (BR)](README.pt_BR.md) | [Español](README.es.md)**

---

# 🎮 Soc Ops – Social Bingo for Networking Events

Break the ice and build real connections with **Soc Ops**, the engaging social bingo game designed for in-person mixers, conferences, and team events. Players roam the venue, find people who match dynamic bingo card prompts, and race to get **5 in a row** while having meaningful conversations.

### 🎯 Why Soc Ops?

- **🤝 Authentic Connections** – Prompts encourage real conversations, not awkward small talk
- **🏃 Engaging Gameplay** – Competitive bingo format keeps energy high throughout the event
- **💻 Modern Web App** – Sleek, mobile-friendly interface built with FastAPI + Jinja2
- **🎲 Customizable** – Generate unique cards with AI-powered prompt generation
- **📊 Real-time Updates** – Live game state and leaderboard tracking

---

## ⚡ Quick Start

### Installation

```bash
# Clone and navigate
git clone https://github.com/copilot-dev-days/my-soc-ops-python
cd my-soc-ops-python

# Install dependencies (requires Python 3.13+)
pip install -e .

# Run the app
soc-ops
```

Visit **http://localhost:8000** and start playing!

---

## 📚 Learn Through Building – Lab Guide

This project includes **comprehensive learning modules** to teach full-stack development, AI integration, and multi-agent systems:

| Part | Title | Focus |
|------|-------|-------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist | Project setup and prerequisites |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering | Repository structure and configuration |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend | UI/UX principles and component design |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master | Building AI-powered prompt generation |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development | Advanced AI orchestration patterns |

> 📝 **Offline Access** – All lab guides are also available in the [`workshop/`](workshop/) folder

---

## 🏗️ Technology Stack

- **Backend** – FastAPI (Python 3.13+)
- **Frontend** – Jinja2 templates + vanilla CSS
- **Database** – In-memory game state (easily extensible)
- **AI** – Customizable prompt generation with Azure OpenAI
- **Testing** – Pytest with full coverage

---

## 📖 Project Structure

```
my-soc-ops-python/
├── app/
│   ├── main.py           # FastAPI application entry point
│   ├── game_logic.py     # Core bingo game mechanics
│   ├── game_service.py   # Game state management
│   ├── models.py         # Data models
│   ├── static/           # CSS and client-side assets
│   └── templates/        # Jinja2 HTML templates
├── tests/                # Pytest test suite
├── workshop/             # Offline lab guide content
└── pyproject.toml        # Project configuration
```

---

## 🎮 How to Play

1. **Start Game** – Create or join a game session
2. **Get Your Card** – Receive a personalized bingo card with 25 unique prompts
3. **Network** – Walk around and find people who match the prompts
4. **Win** – Complete 5 in a row (horizontal, vertical, or diagonal)
5. **Celebrate** – Leaderboard shows your score and completion time

---

## 🚀 Features

✅ **Real-time Card Generation** – Dynamically create bingo cards with AI-powered prompts  
✅ **Multiple Game Modes** – Support for simultaneous players and teams  
✅ **Mobile-Friendly UI** – Play from any device  
✅ **Leaderboard Tracking** – See who's winning in real-time  
✅ **Customizable Prompts** – Tailor questions to your audience  
✅ **Game History** – Review past games and stats

---

## 🤝 Contributing

We welcome contributions! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and pull request process.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 🔗 Resources

- [🚀 Start Learning](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview)
- [📋 Contributing Guide](CONTRIBUTING.md)
- [🛡️ Security Policy](SECURITY.md)
- [💬 Get Support](SUPPORT.md)

---

**Ready to transform your next event?** ✨ Start with [Part 00: Overview](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) and build something amazing with Soc Ops!
