# 📢 Twitter Sentiment Notifier

This project tracks mentions of **Data Science** on Twitter, analyzes the sentiment of tweets using Hugging Face NLP models, and sends alerts for **negative sentiment** directly to a Telegram channel.

🎯 Try it live: [Telegram Alert Channel](https://t.me/sentiment_alert_demo)

---

## 🧠 Features

- ✅ Fetches recent tweets using the Twitter API (filtered by keyword: **Data Science**)
- ✅ Analyzes sentiment using Hugging Face (`twitter-roberta-base-sentiment`)
- ✅ Flags negative tweets and sends them as Telegram alerts
- ✅ Built using the powerful [n8n.io](https://n8n.io) workflow automation tool

---

## ⚙️ Tools & APIs Used

| Tool / Service        | Purpose                            |
|-----------------------|------------------------------------|
| **n8n**               | Workflow automation                |
| **Twitter API**       | Fetch keyword-matching tweets      |
| **Hugging Face API**  | Run sentiment analysis on tweets   |
| **Telegram Bot**      | Send alerts to public Telegram channel |

---




