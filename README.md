# 🤖 AI Customer Support Chatbot

> A production-ready AI customer support system powered by the OpenAI API, featuring session memory, structured JSON responses, smart escalation logic, and full conversation logging.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🧠 Session Memory | Maintains full conversation context per user session |
| 📋 Structured Responses | All replies returned as typed JSON (message, topic, escalation flag) |
| 🚨 Smart Escalation | Auto-detects billing/legal/account queries → routes to human agent |
| 🪵 Logging | All sessions saved to `/sessions/` as JSON; errors logged to `chatbot.log` |
| 🔑 Token Management | Auto-trims history to stay within context window |
| 🔒 Environment-safe | API key loaded from environment variable — never hardcoded |

---

## 🚀 Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/yourprofile/ai-support-chatbot.git
cd ai-support-chatbot

# 2. Install dependencies
pip install openai

# 3. Set your API key
export OPENAI_API_KEY="your-key-here"

# 4. Run the chatbot
python chatbot.py
```

---

## 💬 Example Conversation

```
You: What are your refund policies?
Bot: Refunds are processed within 5–7 business days after approval.

You: I need to cancel my account permanently.
Bot: I'll connect you with a human specialist for that. One moment.
⚠️  Transferring to a human agent...
```

---

## 📁 Project Structure

```
ai-support-chatbot/
├── chatbot.py          # Core chatbot logic
├── requirements.txt    # Dependencies
├── sessions/           # Auto-created — saved session JSON files
├── chatbot.log         # Auto-created — runtime logs
└── README.md
```

---

## 🔧 Configuration

Edit the constants at the top of `chatbot.py`:

| Variable | Default | Description |
|---|---|---|
| `MAX_TOKENS` | `500` | Max tokens per response |
| `MAX_HISTORY` | `10` | Message pairs to retain in context |
| `SYSTEM_PROMPT` | (see file) | Bot personality and FAQ knowledge base |

---

## 🛠️ Built With

- Python 3.10+
- OpenAI API (`gpt-4o-mini`)
- Standard library: `json`, `logging`, `uuid`, `os`

---

## 👤 Author

**Arinze Emelobe** — AI Automation & Training Specialist  
[LinkedIn](https://linkedin.com/in/yourprofile) · [GitHub](https://github.com/yourprofile) · [Email](mailto:arinzeemelobe17@gmail.com)
