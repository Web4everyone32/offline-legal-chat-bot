# 🤖 Niglen — Offline AI Legal Chatbot v2.1

A fully offline, privacy-first AI chatbot specialized in Indian law, with PDF document intelligence. Built with Node.js, React, and Ollama — no cloud, no API keys, no data leaving your machine.

---

## ✨ Features

- 🔒 **100% Offline** — All AI inference runs locally via Ollama
- ⚖️ **Indian Legal Assistant** — Specialized in IPC, Constitution, Consumer Law, Contract Law
- 📄 **PDF Chat (RAG)** — Upload legal documents and ask questions grounded in their content
- 💾 **Persistent Storage** — PDFs and conversations saved permanently across restarts
- ⚡ **Streaming Responses** — Tokens stream in real time as the AI thinks
- 🌍 **Multilingual** — Auto-detects language; supports English, Tamil, Hindi, Malayalam, French, Spanish, German, Japanese
- 🌙 **Dark Mode** — Toggle between light and dark themes
- 📁 **Document Manager** — View and remove uploaded PDFs per session
- 💬 **Multi-conversation** — Manage multiple chat sessions from the sidebar
- 🛡️ **Safety Guardrails** — Built-in content filtering, refuses non-legal questions
- 📝 **Markdown Rendering** — Responses render bold, lists, code blocks, and headers

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 + Vite |
| Backend | Node.js + Express |
| AI Runtime | Ollama (local) |
| Chat Model | legal-bot (LLaMA 3 fine-tuned via Modelfile) |
| Embedding Model | nomic-embed-text |
| Vector Search | Cosine similarity (in-memory) |
| PDF Parsing | pdf-parse |
| Persistent Storage | JSON file (storage.json) |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) v18+
- [Ollama](https://ollama.com/download)

### 1. Install Ollama & pull models

```bash
ollama serve
```

In a new terminal:

```bash
ollama pull llama3
ollama pull nomic-embed-text
```

### 2. Create the legal-bot model

```bash
cd server
ollama create legal-bot -f Modelfile
```

### 3. Start the backend

```bash
cd server
npm install
copy .env.example.env .env
npm run dev
```

Server runs on → `http://localhost:8080`

### 4. Start the frontend

```bash
cd web
npm install
npm run dev
```

App runs on → `http://localhost:5173`

---

## 📄 Recommended Legal PDFs to Upload

| Document | Source |
|----------|--------|
| Indian Penal Code (IPC) | indiacode.nic.in |
| Constitution of India | legislative.gov.in |
| Consumer Protection Act 2019 | consumeraffairs.nic.in |
| Indian Contract Act 1872 | indiacode.nic.in |
| IT Act 2000 | meity.gov.in |

> PDFs are saved permanently via `storage.json` — upload once, use forever.

---

## 📁 Project Structure
