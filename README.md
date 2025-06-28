\# 📢 Twitter Sentiment Notifier



This project tracks mentions of \*\*HR Software\*\* on Twitter, analyzes the sentiment of tweets using Hugging Face NLP models, and sends alerts for \*\*negative sentiment\*\* directly to a Telegram channel.



> 🚨 Try it live: \[Telegram Alert Channel](https://t.me/sentiment\_alert\_demo)



---



\## 🧠 Features



\- ✅ Fetches recent tweets using the Twitter API (filtered by keyword: \*\*HR Software\*\*)

\- ✅ Analyzes sentiment using Hugging Face (`twitter-roberta-base-sentiment`)

\- ✅ Flags negative tweets and sends them as Telegram alerts

\- ✅ Built using the powerful \[n8n.io](https://n8n.io) workflow automation tool



---



\## ⚙️ Tools \& APIs Used



| Tool / Service | Purpose |

|----------------|---------|

| \*\*n8n\*\*        | Workflow automation |

| \*\*Twitter API\*\*| Fetching tweets by keyword |

| \*\*Hugging Face\*\*| Sentiment classification |

| \*\*Telegram Bot\*\*| Alert delivery |

| \*\*Docker\*\*     | Self-hosted n8n instance |



---



\## 📌 Telegram Notification Example



!\[telegram-demo](https://user-images.githubusercontent.com/your-id/demo-image-placeholder.png)  

> "🚨 Alert: HR systems are broken and frustrating to use"



---



\## 📂 Workflow Overview



```plaintext

\[Trigger / Timer Node]

&nbsp;       ↓

\[HTTP Request: Twitter API]

&nbsp;       ↓

\[Function Node: Format Tweets]

&nbsp;       ↓

\[HTTP Request: Hugging Face Sentiment]

&nbsp;       ↓

\[Function Node: Map Sentiment Label]

&nbsp;       ↓

\[IF Node: Check for NEGATIVE]

&nbsp;      ↙      ↘

\[Send Alert 🟢]   \[Do Nothing 🔴]



