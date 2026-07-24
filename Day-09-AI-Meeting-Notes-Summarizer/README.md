# 📝 Day 09 - AI Meeting Notes Summarizer

## 📌 Project Overview

An AI-powered Meeting Notes Summarizer built using n8n and OpenAI.

The workflow converts raw meeting conversations into professional meeting minutes including:

- Executive Summary
- Discussion Points
- Decisions
- Action Items
- Pending Tasks
- Risks
- Deadlines
- Next Meeting
- Overall Outcome

Perfect for project managers, team leads and corporate meetings.

---

## 🛠 Tech Stack

- n8n
- OpenAI GPT
- AI Agent
- Webhook Response
- Markdown Formatting

---

## Workflow

Chat Input

↓

AI Agent

↓

OpenAI GPT

↓

Professional Meeting Report

---

## Nodes Used

### 1. When Chat Message Received

Receives meeting transcript.

---

### 2. AI Agent

Analyzes the transcript and creates a structured report.

---

### 3. OpenAI Chat Model

Generates the final meeting summary.

---

### 4. Respond to Webhook

Displays the report inside the chat.

---

## Features

✅ Executive Summary

✅ Main Discussion Points

✅ Decisions Taken

✅ Action Items

✅ Pending Tasks

✅ Risks & Concerns

✅ Deadlines

✅ Next Meeting

✅ Overall Outcome

---

## Sample Input

Rahul:
Website deployment should finish by Friday.

Abhishek:
Testing is completed.

Rohit:
Need client approval before deployment.

Manager:
Let's schedule another meeting on Monday.

---

## Sample Output

📋 Executive Summary

📝 Meeting Summary

💬 Main Discussion Points

✅ Decisions Taken

🎯 Action Items

⏳ Pending Tasks

⚠️ Risks

📅 Deadlines

🔄 Next Meeting

📌 Overall Outcome

---

## Learning

- AI Prompt Engineering
- Markdown Formatting
- Meeting Summarization
- Business Documentation
- AI Report Generation

---

## Future Improvements

- PDF Export

- Email Meeting Minutes

- Google Docs Integration

- Notion Integration

- Slack Notification

- Calendar Reminder

- Speaker Detection

- Audio Meeting Transcription

---

## Project Status

✅ Completed
