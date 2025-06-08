# 🧠 JellyCable

**Your terminal. Smarter. Local. Hackable. Open.**

JellyCable is an open-source CLI tool that acts as your AI pair programmer — like Claude Code or Copilot, but runs in your terminal, supports any model, and works even offline.

---

## ✨ Features

- 🧠 **Run with any LLM**: OpenAI, Claude, Ollama, custom APIs
- 🔌 **LangChain + LangGraph support**: Build custom tools, agents, workflows
- 📂 **Reads your codebase**: With `.gitignore` or `.jcignore` support
- 🧬 **AST-safe edits**: Uses `libcst` for Python or prompt-diffing for others
- 🧠 **Memory & search**: Store context in SQLite or ChromaDB
- 🎛️ **Configurable**: Choose provider, model, temperature via CLI
- 📦 **Single binary (coming soon)**: Easy to install and run anywhere

---

## 🚀 Getting Started

```bash
# Clone
git clone https://github.com/yourname/jellycable
cd jellycable

# Setup
pip install -r requirements.txt

# Run
python jellycable.py
