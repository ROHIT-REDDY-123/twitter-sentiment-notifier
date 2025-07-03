# 📢 Tweet Sentiment Telegram Notifier

This n8n workflow analyzes the sentiment of tweets related to **Data Science** using Hugging Face’s NLP model and sends structured sentiment results to a **Telegram channel**.

---

## ⚙️ Workflow Overview

> Manual Trigger → Twitter API → Tweet Extractor → Hugging Face Sentiment API → Sentiment Classifier → Merge Data → Telegram

---

## 🔧 How It Works

1. **Manual Trigger**
   - Starts the workflow when you click “Execute workflow”.

2. **Twitter API**
   - Fetches recent tweets containing the keyword `"Data Science"` using Twitter API v2.
   - Returns tweet metadata including text, author ID, and timestamp.

3. **Tweet Extractor**
   - Extracts `text`, `created_at`, and `author_id` from each tweet using a code node.

4. **Hugging Face Sentiment API**
   - Sends tweet text to the model `cardiffnlp/twitter-roberta-base-sentiment`.
   - Returns sentiment labels (LABEL_0, LABEL_1, LABEL_2) with confidence scores.

5. **Sentiment Classifier**
   - Maps model output labels:
     - `LABEL_0 → NEGATIVE`
     - `LABEL_1 → NEUTRAL`
     - `LABEL_2 → POSITIVE`
   - Picks the top label based on highest score.

6. **Code (Data Merger)**
   - Combines tweet metadata and sentiment result into one message object.

7. **Send to Telegram**
   - Sends each tweet's details and sentiment result as a message to a Telegram channel using the Telegram Bot API.

---

## 📦 Dependencies

- [n8n](https://n8n.io/) (self-hosted or desktop)
- Twitter Developer Account with Bearer Token
- Hugging Face API Token (free tier works)
- Telegram Bot Token and Channel

---


