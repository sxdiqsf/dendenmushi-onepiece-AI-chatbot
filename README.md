# dendenmushi-onepiece-AI-chatbot
🐌 AI-powered One Piece oracle — ask anything about characters, Devil Fruits, Haki &amp; Grand Line lore. Built with RAG, FAISS, Groq Llama 3.1 &amp; Flask. Try it free at dendenmushi.space

<div align="center">

<img src="frontend/og-image.png" alt="Den Den Mushi — One Piece AI Oracle" width="100%"/>

# 🐌 Den Den Mushi — One Piece AI Oracle

**Ask anything about One Piece — characters, Devil Fruits, Haki, arcs, and Grand Line lore.**  
Powered by RAG (Retrieval-Augmented Generation) + Groq Llama 3.1 70B.

[![Live](https://img.shields.io/badge/Live%20Demo-dendenmushi.space-D70000?style=for-the-badge&logo=google-chrome&logoColor=white)](https://dendenmushi.space)
[![Ko-fi](https://img.shields.io/badge/Support-Ko--fi-29ABE0?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/sadiisaihouse)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## ✨ Features

- 🧠 **RAG Pipeline** — FAISS vector search over a curated One Piece knowledge base (Chapters 1–1055)
- ⚡ **Groq Llama 3.1 70B** — fast, high-quality answers in Den Den Mushi's voice
- 🎨 **Immersive UI** — animated ocean background, Thousand Sunny ship, Straw Hat crew SVGs
- 📱 **Mobile-friendly** — fully responsive design
- 💬 **Conversational memory** — remembers context across your chat session
- 🏴‍☠️ **In-character responses** — answers as a One Piece encyclopedia crewmate
- 🇮🇳 **UPI + Ko-fi + Buy Me a Coffee** — support options for fans

---

## 🛠️ Tech Stack

| Layer | Tech |
|---|---|
| **LLM** | Groq API — Llama 3.1 70B Versatile |
| **Embeddings** | `sentence-transformers` — all-MiniLM-L6-v2 |
| **Vector DB** | FAISS |
| **Backend** | Python · Flask · Flask-CORS |
| **Frontend** | Vanilla JS · HTML5 · CSS3 · SVG |
| **Deployment** | Railway · Custom domain via Cloudflare |

---

## 🗂️ Project Structure

```
dendenmushi/
├── backend/
│   ├── app.py              # Flask API — /api/chat, /api/track, /api/health
│   ├── requirements.txt
│   └── .env.example
├── frontend/
│   ├── index.html          # Single-page app
│   ├── og-image.png        # Social preview image
│   └── qr.jpg              # UPI QR code
├── data/
│   ├── index.faiss         # FAISS vector index
│   └── chunks.pkl          # Text chunks
├── scripts/
│   └── update_index.py     # Rebuild the vector index
├── deploy/
│   ├── DEPLOY_GUIDE.md
│   └── setup.sh
├── Procfile
└── runtime.txt
```

---

## 🚀 Running Locally

**1. Clone the repo**
```bash
git clone https://github.com/sxdiqsf/dendenmushi.git
cd dendenmushi
```

**2. Set up environment**
```bash
cp .env.example .env
# Fill in your GROQ_API_KEY in .env
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Run the backend**
```bash
cd backend
python app.py
```

**5. Open in browser**
```
http://localhost:5000
```

---

## ⚙️ Environment Variables

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | Your Groq API key — [get one free](https://console.groq.com) |
| `GIST_ID` | GitHub Gist ID for visitor analytics |
| `GITHUB_TOKEN` | GitHub token with `gist` scope only |
| `GROQ_MODEL` | Default: `llama-3.1-70b-versatile` |
| `TOP_K` | Number of chunks to retrieve (default: 6) |

---

## 🌊 Deployment (Railway)

```bash
# Push to GitHub — Railway auto-deploys
git add .
git commit -m "your message"
git push
```

Set these in Railway → Variables:
```
GROQ_API_KEY=your_key
GIST_ID=your_gist_id
GITHUB_TOKEN=your_token
```

---

## ☕ Support

Den Den Mushi is free forever. If it helped you on your Grand Line journey:

[![Ko-fi](https://img.shields.io/badge/Ko--fi-sadiisaihouse-29ABE0?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/sadiisaihouse)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-sadiqaihouse-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/sadiqaihouse)

---

<div align="center">

*One Piece © Eiichiro Oda / Shueisha / Toei Animation — Fan-made project, not affiliated.*

⚓ **Fair winds and following seas.** ⚓

</div>
