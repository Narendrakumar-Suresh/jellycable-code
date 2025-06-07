# Todo

## ✅ **Model Code: Updated Stack**

* **LangChain (JS)**: for agents, tools, chains
* **LangGraph (JS)**: for graph-based flows (e.g., planner → coder → executor)
* **CLI**: `commander`, `inquirer`, `chalk`
* **SQLite**

---

## 🧭 Updated Todo Plan (with LangChain + LangGraph)

### 📁 Phase 1: Setup + Basic CLI

* [ ] `npm install langchain langgraph`
* [ ] Setup CLI using `inquirer` or `commander`
* [ ] Load `.env` with `OPENAI_API_KEY`

---

### ⚙️ Phase 2: Providers (OpenAI, Ollama)

* [ ] Create LangChain `ChatOpenAI` instance
* [ ] Create custom Ollama wrapper (LangChain doesn’t have native Ollama yet, use `axios`)
* [ ] Abstract model selection

```ts
// lib/models.ts
export function getModel(provider: 'openai' | 'ollama') {
  // Return ChatOpenAI or custom wrapper
}
```

---

### 🧠 Phase 3: Agent & LangGraph

* [ ] Create base agent using LangChain
* [ ] Build a LangGraph with nodes:

  * `user_input`
  * `model_response`
  * `tool_executor` (optional)
* [ ] Setup a basic loop like Claude Code (prompt → response → optional tool)

---

### 🧰 Phase 4: Add Tools (Optional)

* [ ] Add code executor tool (JS)
* [ ] Add file I/O tool (load file into prompt context)
* [ ] Optional: LangChain tool agent

---

### 💾 Phase 5: History & Config

* [ ] Save chat history to file
* [ ] Store preferred model in `.modelcoderc.json`

---

### 📦 Final: Package It

* [ ] Build `.exe` using `pkg` or `nexe`

---

## 🧠 Sample LangGraph Flow

```
[user_input]
     ↓
[model_call (OpenAI/Ollama)]
     ↓
[check for tools]
     ↓
[execute_tool_if_needed]
     ↓
[return response → CLI]
```

---
