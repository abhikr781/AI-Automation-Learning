# 🤖 Day 05 - AI Agent with Memory & Tools (n8n + Groq)

## 📌 Project Overview

Today I built my first AI Agent using **n8n** and **Groq LLM**.

Unlike a normal chatbot, this AI Agent can:

- Remember previous conversations
- Use external tools automatically
- Choose the correct tool based on the user's query
- Respond in natural language

This project helped me understand the core concepts of **AI Agents**, **Memory**, and **Tool Calling**.

---

## 🛠️ Tech Stack

- n8n
- Groq Chat Model
- AI Agent Node
- Chat Trigger
- Simple Memory
- Calculator Tool
- Date & Time Tool
- Wikipedia Tool

---

## 🏗️ Workflow Architecture

```text
                    User
                      │
                      ▼
               Chat Trigger
                      │
                      ▼
                 AI Agent
          ┌──────────┼───────────┐
          │          │           │
          ▼          ▼           ▼
      Groq LLM   Simple Memory   Tools
                                 │
               ┌─────────────────┼─────────────────┐
               ▼                 ▼                 ▼
          Calculator        Date & Time      Wikipedia
```

---

## 🚀 Features

- ✅ Conversational AI Agent
- ✅ Conversation Memory
- ✅ Automatic Tool Selection
- ✅ Mathematical Calculations
- ✅ Current Date & Time
- ✅ Wikipedia Search
- ✅ Natural Language Responses

---

## 🧠 What I Learned

- Difference between Chatbot and AI Agent
- AI Agent Architecture
- LLM Integration
- Memory Handling
- Tool Calling
- Prompt Engineering Basics
- Decision Making using AI Agent
- Building AI Workflows with n8n

---

## 🧪 Test Cases

### 🧠 Memory Test

**Input**

```
My name is Abhishek.
```

**Output**

```
Your name is Abhishek.
```

---

### 🧮 Calculator Tool

**Input**

```
45 × 20
```

**Output**

```
900
```

---

### 📅 Date & Time Tool

**Input**

```
What's today's date?
```

**Output**

```
20 July 2026
```

---

### 📚 Wikipedia Tool

**Input**

```
Tell me about Dr. A.P.J. Abdul Kalam
```

**Output**

```
AI automatically used the Wikipedia Tool and generated a summary.
```

---

## 📸 Workflow Screenshot

> Add your workflow screenshot here.

Example:

```
images/day05-ai-agent-workflow.png
```

---

## 📂 Project Structure

```text
Day-05-AI-Agent/
│
├── README.md
├── workflow.json
└── images/
    └── day05-ai-agent-workflow.png
```

---

## 🎯 Future Improvements

- Web Search Integration
- PDF Reader
- Gmail Integration
- Google Sheets Integration
- Telegram Bot
- Database Integration
- Multi-Agent Workflow

---

## 📚 Key Concepts Covered

- AI Agent
- LLM
- Memory
- Tool Calling
- Workflow Automation
- Prompt Engineering
- AI Orchestration

---

## 👨‍💻 Author

**Abhishek Kumar**

Learning AI Automation Engineering one project at a time 🚀

GitHub Repository:

https://github.com/abhikr781/AI-Automation-Learning
