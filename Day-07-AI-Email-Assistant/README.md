# 📧 Day 07 - AI Email Assistant using n8n + OpenAI

## 📌 Project Overview

An AI-powered Email Writing Assistant built using **n8n** and **OpenAI GPT**.

The assistant accepts a user's request in natural language and generates a professional email in seconds.

Example:

**User Input**

> Write a leave application for 3 days because of fever.

**AI Output**

- Subject
- Greeting
- Email Body
- Closing
- Signature

---

# 🛠 Tech Stack

- n8n
- OpenAI Chat Model (GPT-4.1 Mini)
- AI Agent
- Simple Memory

---

# 🚀 Workflow

```
Chat Trigger
      │
      ▼
AI Agent
      │
      ▼
OpenAI Chat Model
      │
      ▼
Professional Email Response
```

---

# 🤖 AI Prompt Used

```
You are an expert Email Writing Assistant.

Your task is to generate professional, well-formatted emails.

Rules:

- Understand the user's request.
- Generate a relevant subject.
- Add a professional greeting.
- Write a clear email body.
- Add a polite closing.
- Add an appropriate signature.
- Keep the language simple and professional.
- Never explain your reasoning.
- Return only the final email.
```

---

# 🧪 Example 1

### User

```
Write a leave application for 3 days because of fever.
```

### Output

```
Subject: Leave Application Due to Illness

Dear Manager,

I hope you are doing well.

I am writing to request leave for three days due to fever. My doctor has advised complete rest.

I kindly request leave from Monday to Wednesday. I will ensure all pending work is completed after returning.

Thank you for your understanding.

Best Regards,
Your Name
```

---

# 🧪 Example 2

### User

```
Write an email requesting work from home for one week.
```

### Output

Professional Work From Home Email

---

# 🧪 Example 3

### User

```
Write a resignation email.
```

### Output

Professional resignation email with proper formatting.

---

# 📚 What I Learned

- Creating AI Agents in n8n
- Using OpenAI Chat Model
- Writing effective System Prompts
- Prompt Engineering basics
- Structuring AI responses
- Creating reusable AI workflows
- Testing different user inputs
- Improving AI output quality using prompts

---

# 💡 Future Improvements

- Gmail Integration
- Outlook Integration
- Send Email automatically
- Email Templates
- Tone Selection
- Formal / Friendly modes
- Multi-language support
- Grammar correction
- AI Email Reply Generator
- Save generated emails to Google Docs
- Slack Notification
- Microsoft Teams Integration

---

# 🎯 Skills Practiced

- n8n
- AI Agents
- OpenAI API
- Prompt Engineering
- Workflow Automation
- LLM Applications

---

# 📸 Project Screenshot

(Add your workflow screenshot here)

---

# 👨‍💻 Author

Abhishek Kumar

Learning AI Automation • n8n • OpenAI • Workflow Automation

Day 07 Complete ✅
