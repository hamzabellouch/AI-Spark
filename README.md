# ⚡ AI Spark - Local Multi-Model AI Orchestrator

AI Spark is a local FastAPI web interface that allows you to simultaneously broadcast a query to multiple AI chat interfaces (ChatGPT, Gemini, DeepSeek) running inside your own web browser (Brave, Chrome, Edge, Firefox), view and compare their results side-by-side in a beautiful grid layout, and generate a unified, synthesized response via Claude.

Because it controls your local web browser directly, **AI Spark is 100% private, free, and does not require paid API keys**. It leverages your existing browser logins, cookies, and active sessions.

---

## 🎨 Key Features

*   ⚡ **Simultaneous Broadcast:** Write one prompt and send it to ChatGPT, Gemini, and DeepSeek concurrently.
*   🖥️ **Comparison Grid:** Compare answers side-by-side in a modern, responsive layout that automatically adjusts to the number of active models.
*   🧠 **Claude Synthesis:** Automatically feed all collected answers into Claude to generate a unified, highly detailed, and optimized synthesis.
*   📁 **Local History & Sessions:** Save and search past conversations locally via a lightweight SQLite database.
*   🌍 **Multi-Language & RTL:** Built-in support for Arabic, English, and French, with automatic LTR/RTL switching.
*   🌓 **Premium UI/UX:** Responsive dark/light theme, modern typography (Tajawal & Inter), and animated splash screen.

---

## 🛠️ System Requirements

1.  **Python 3.11** or newer.
2.  **Playwright** library (installed automatically on startup).
3.  Any supported browser installed on your machine:
    *   **Brave Browser** (Recommended)
    *   **Google Chrome**
    *   **Microsoft Edge**
    *   **Mozilla Firefox**

---

## 🚀 Quick Start & Setup

To run the application, choose the launcher script corresponding to your operating system:

*   **Windows:** Double-click [run_windows.bat](file:///E:/AI%20spark/run_windows.bat). See the [Windows User Guide](file:///E:/AI%20spark/WINDOWS.md) for more details.
*   **macOS:** Double-click [run_macos.command](file:///E:/AI%20spark/run_macos.command). See the [macOS User Guide](file:///E:/AI%20spark/MACOS.md) for more details.
*   **Linux:** Execute [run_linux.sh](file:///E:/AI%20spark/run_linux.sh). See the [Linux User Guide](file:///E:/AI%20spark/LINUX.md) for more details.

On startup, the script will automatically install dependencies from `requirements.txt`, launch your selected browser in remote debugging mode (reusing your daily cookies and sessions), and open the dashboard at `http://127.0.0.1:8000`.

---

## 📁 Repository Structure

*   `main.py` - FastAPI backend server.
*   `browser.py` - Browser controller via Playwright and Chrome DevTools Protocol (CDP).
*   `agents.py` - Agent automation scripts for prompt typing and submission.
*   `utils.py` - DOM parsing and scraping utility functions.
*   `db.py` - Database initialization and session management.
*   `static/` - Stylesheets (`style.css`), app logic (`app.js`), and logo icons.
*   `templates/` - HTML index layout template.

---

## 🔒 Privacy & Security

AI Spark runs 100% locally. The codebase **does not** collect, store, or transmit your credentials, cookies, or browser profiles to any external servers. Your chat history is saved in a local SQLite file (`chat_history.db`) on your own computer.
