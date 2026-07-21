# 🚀 Day 06 - AI HTTP News Agent using n8n

An AI-powered News Agent built using **n8n**, **OpenAI**, and the **HTTP Request Tool**.

The agent understands natural language, calls an external News API in real time, and summarizes the latest news in a clean and user-friendly format.

---

# 📌 Project Overview

This project demonstrates how an AI Agent can interact with external REST APIs to fetch live information.

The workflow extracts the user's request, sends it to a News API using an HTTP Request Tool, and allows the AI model to summarize the response before displaying it to the user.

This is a practical example of combining **LLMs + APIs + Automation**.

---

# 🛠️ Tech Stack

- n8n
- OpenAI Chat Model
- HTTP Request Tool
- MarketAux News API
- Simple Memory

---

# ⚙️ Workflow

```
User Message
      │
      ▼
AI Agent
      │
      ├──────────────► OpenAI Chat Model
      │
      ├──────────────► HTTP Request Tool
      │                      │
      │                      ▼
      │             MarketAux News API
      │
      ▼
AI Summarizes Response
      │
      ▼
Formatted News Output
```

---

# ✨ Features

✅ AI-powered conversation

✅ Dynamic HTTP API Integration

✅ Real-time News Fetching

✅ AI Tool Calling

✅ Automatic News Summarization

✅ Source & Published Date

✅ Read More Link

✅ Memory Support

---

# 📸 Example User Prompts

### Example 1

```
Share the latest news
```

### Example 2

```
Latest news about Apple
```

### Example 3

```
Tell me the latest news about Tata Motors
```

### Example 4

```
Show AI related latest news
```

---

# 📥 Example Output

```
📰 Latest News

Title:
Apple launches new AI features

Summary:
Apple introduced new AI capabilities across its ecosystem,
bringing smarter Siri and productivity improvements.

Source:
Reuters

Published:
21 July 2026

Read More:
https://example.com
```

---

# 🧠 What I Learned

- Building AI Agents in n8n
- Using OpenAI with n8n
- Connecting AI with external APIs
- Working with HTTP Request Tool
- Dynamic Tool Calling
- REST API Integration
- Prompt Engineering
- Formatting API Responses
- Building Real-world AI Workflows

---

# 🚧 Challenges Faced

While building this project, I tested multiple News APIs.

Some free APIs returned outdated articles due to free-tier limitations.

After experimenting with different providers, I successfully integrated a News API that returns recent news and allows dynamic searches.

This project also helped me understand how API limitations affect real-world AI applications.

---

# 📁 Project Structure

```
Day-06-AI-HTTP-Agent
│
├── README.md
├── workflow.json
└── screenshots
      ├── workflow.png
      └── output.png
```

---

# 📷 Workflow Screenshot

> Add your workflow screenshot here.

---

# 🚀 Future Improvements

- Stock Market News Agent
- News Sentiment Analysis
- Multiple News Sources
- Company Ticker Detection
- Stock News API Integration
- Telegram Notification
- Discord Bot
- Daily AI News Digest
- Email Alerts
- Portfolio Tracker Integration

---

# 💡 Key Takeaway

This project demonstrates how an AI Agent can interact with external APIs to retrieve live information and convert raw API responses into meaningful, user-friendly summaries.

It is a strong foundation for building more advanced AI Automation projects such as Financial AI Agents, Research Assistants, Customer Support Bots, and AI-powered Workflow Automation.

---

# 🎯 Learning Outcome

By completing this project, I gained hands-on experience with:

- AI Agents
- OpenAI Integration
- HTTP APIs
- REST API Communication
- Tool Calling
- Dynamic AI Workflows
- Real-world Automation using n8n

---

# ✅ Project Status

- ✔ AI Agent Created
- ✔ OpenAI Connected
- ✔ HTTP Request Tool Integrated
- ✔ News API Connected
- ✔ Dynamic Query Handling
- ✔ AI Summarization
- ✔ Memory Enabled
- ✔ Day 06 Completed

---

## ⭐ Connect With Me

If you found this project helpful, feel free to ⭐ the repository.

I'm currently learning **AI Automation, n8n, LLMs, OpenAI, RAG, and AI Agents** while building practical real-world projects every day.

Stay tuned for more AI Automation projects 🚀
